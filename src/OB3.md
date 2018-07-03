# 0B3

This page documents the `.ob3` format, a bespoke format for 3D models
created by Jagex.
It is used by the RuneScape Classic engine since client version
\#74.

Note: There is also an earlier version of this format called `.ob2`.

## OB3 Model Class
The following is the fully renamed client code used to represent OB3 models.

```java
public class OB3Model {

    private static final int num_seq = 0xbc614e; // 12345678
    public int vertex_count;
    public int vertices_x[];
    public int vertices_y[];
    public int vertices_z[];
    public int face_count;
    public int face_vertex_count[];
    public int face_vertices[][];
    public int face_fill_back[];
    public int face_fill_front[];
    public int face_gouraud[];

    public OB3Model(byte data[], int offset) {
        int vertex_count = get_uint16(data, offset);
        offset += 2;
        int face_count = get_uint16(data, offset);
        offset += 2;

        vertices_x = new int[vertex_count];
        vertices_y = new int[vertex_count];
        vertices_z = new int[vertex_count];
        face_vertex_count = new int[face_count];
        face_vertices = new int[face_count][];
        face_fill_back = new int[face_count];
        face_fill_front = new int[face_count];
        face_gouraud = new int[face_count];

        for (int v = 0; v < vertex_count; v++) {
            vertices_x[v] = get_int16b(data, offset);
            offset += 2;
        }

        for (int v = 0; v < vertex_count; v++) {
            vertices_y[v] = get_int16b(data, offset);
            offset += 2;
        }

        for (int v = 0; v < vertex_count; v++) {
            vertices_z[v] = get_int16b(data, offset);
            offset += 2;
        }

        this.vertex_count = vertex_count;
        for (int f = 0; f < face_count; f++)
            face_vertex_count[f] = get_ubyte(data[offset++]);

        for (int f = 0; f < face_count; f++) {
            face_fill_back[f] = get_int16b(data, offset);
            offset += 2;
            if (face_fill_back[f] == 32767)
                face_fill_back[f] = num_seq;
        }

        for (int f = 0; f < face_count; f++) {
            face_fill_front[f] = get_int16b(data, offset);
            offset += 2;
            if (face_fill_front[f] == 32767)
                face_fill_front[f] = num_seq;
        }

        for (int f = 0; f < face_count; f++) {
            int i = get_ubyte(data[offset++]);
            if (i == 0)
                face_gouraud[f] = 0;
            else
                face_gouraud[f] = num_seq;
        }

        for (int f = 0; f < face_count; f++) {
            face_vertices[f] = new int[face_vertex_count[f]];
            for (int fv = 0; fv < face_vertex_count[f]; fv++) {
                if (vertex_count < 256) {
                    face_vertices[f][fv] = get_ubyte(data[offset++]);
                } else {
                    face_vertices[f][fv] = get_uint16(data, offset);
                    offset += 2;
                }
            }
        }

        this.face_count = face_count;
    }

    private static int get_ubyte(byte b) {
        return (b & 0xff);
    }

    private static int get_uint16(byte b[], int start) {
        return (get_ubyte(b[start]) << 8) + get_ubyte(b[start + 1]);
    }

    private static int get_int16b(byte b[], int start) {
        int i = get_ubyte(b[start]) * 256 + get_ubyte(b[start + 1]);
        if (i > 32767)
            i -= 0x10000;
        return i;
    }
}
```

## Faces

A negative face_fill_back or face_fill_front value indicates a solid colour, whereas a positive value indicates a texture.
The texture is defined by its offset in the client's texture array.

When converting to/from [Wavefront OBJ](https://en.wikipedia.org/wiki/Wavefront_.obj_file)
format, remember that the OB3 face vertices are one less than the OBJ
face vertices.

The below code will allow you to encode or decode colours in this format.

```java
public static int decode_colour(int i) {
    i = -(i + 1);
    int r = i >> 10 & 0x1f;
    int g = i >> 5 & 0x1f;
    int b = i & 0x1f;
    return (r << 19) + (g << 11) + (b << 3);
}

public static int encode_colour(int r, int g, int b) {
    return -1 - (r / 8) * 1024 - (g / 8) * 32 - b / 8;
}
```

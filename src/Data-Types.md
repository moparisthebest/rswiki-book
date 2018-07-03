# Data types

RuneScape uses a number of common and bespoke data types in the
process of data transmission.

## Byte Order

Data types that are two bytes or larger can be stored and ordered in a
variety of different ways.
The traditional byte orders are big endian and little endian.
Generally people either use big endian or little endian.

RuneScape uses both little and big-endian byte orders throughout the
protocol (however, the 194 client only uses big-endian order).
This presumably to make reverse-engineering of the protocol harder.

Note: Some confusion has arisen over the byte order as the data types
are named incorrectly in Winterlove's server where little endian data
types are incorrectly named as big endian types.

### Big Endian

In big endian order, the most significant byte (MSB) is stored first and
the least significant byte (LSB) is stored last.

### Little Endian

In little endian order, the least significant byte (LSB) is stored first
and the most significant byte (MSB) is stored last.

## Bespoke Byte Orders

Additionally, RuneScape also uses two endian orders for integers that
are different from a big- or low endian order.
We call these byte orders middle endian.

### Middle Endian Big Int

The bytes are stored in the following order, where A1 is the smallest byte (I.e. LSB) and D4 the bigger (i.e. MSB): C3 D4 A1 B2.

### Middle Endian Small Int

The bytes are stored in the following order, where A1 is the smallest byte (I.e. LSB) and D4 the bigger (i.e. MSB): B2 A1 D4 C3.

## Common data types

These data types are traditional, hence they can typically be written
and read by a standard DataStream, or Buffer implementation.

Naming conventions:

| Standardized name | Data-type name | Jagex name | Encoding |
|---|---|---|---|
| Byte | byte | 1,1b | Bytes |
| [Word](./Word.md) | short | 2,2b | Bytes |
| [DWord](./DWord.md) | int, int32 | 2,2b | Bytes |
| [QWord](./QWord.md) | long, int64 | 8,8b | Bytes |
| C-style String | string, String, char*, char[] | str, strbyte | Text bytes followed by `\n` or the byte `10`. |
| Java-string String | string, String, char*, char[] | strraw | Length as a word, followed by the text bytes. |

Note: In more recent versions of the client, C-style strings are terminated with the null character (i.e. `\0`) or the byte `0` to support multi-line strings.

## Bespoke data types

These data types are bespoke, that is, they were developed with the
sole intention of only being used within Jagex products.

We presume that this is another technique employed to make
reverse-engineering and packet manipulation harder.

Naming conventions:

| Winterlove's name | Jagex name | Read transformation | Write transformation |
|---|---|---|---|
| Special A | Unknown | value - 128 | value + 128 |
| Special C | Unknown | 0 - value | 0 - value |
| Special S | Unknown | 128 - value | 128 - value |
| SpaceSaverA | smarts | `(value[0] < 128) ? (((value[0] - 128) << 8) + value[1]) : value[0]` | `if(value < 128) putword(value+32768) else putbyte(value);` |
| SpaceSaverB | smart | `(value[0] << 24) + (value[1] << 16) + value[2] ` | `putbyte(value >> 24); putbyte(value >> 16); putbyte(value); ` |
| Tribyte, RGBColour, 3Byte, int3, medium | 3 | `(value[0] << 24) + (value[1] << 16) + value[2]` | `putbyte(value >> 24); putbyte(value >> 16); putbyte(value); ` |
| [RS String](./RS-String.md) | jstr | Old engine: read until newline terminated ("\n"). New engine: read until null byte (value 0). | Old engine: write and finish with newline delimiter ("\n"). New engine: write and finish with null byte (value 0).  |

Note: The read transformation is the process which must be applied to
read data, to reconstruct the original.
The write transformation applies analogously, to when data is written.

## Bit Access

### Initiating Bit Access

Whenever data is to be sent to the server or to the client using bits;
the stream needs to be prepared by setting the bit position.
The bit position can be calculated by multiplying the current buffer
position by 8. This is because each byte is comprised of 8 bits.

e.g. `int bitPos = bufferPos * 8;`

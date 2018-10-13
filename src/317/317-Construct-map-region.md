# Construct Map Region
The construct map region packet sends a dynamic map region that is constructed by using groups of 8x8 tiles.
It is generally used for instanced areas, such as fight caves, and in later revisions, player owned houses.

## Packet Details
| Key | Value |
|--|--|
| Name | Construct map region |
| Description | Constructs a new map region from a palette of 8x8 tiles. |
| Opcode | 241 |
| Type | Variable Short |
| Length | N/A |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The region Y coordinate (absolute Y coordinate / 8), plus 6. |
| Bit block | See below. |
| [Short](/Data-Types.html#common-data-types) | The region X coordinate (absolute X coordinate / 8), plus 6. |

## Bit block
The bit block contains the 'palette' of map regions to make up the new region.

A loop is used to construct it, as follows:

```java
for (int z = 0; z < 4; z++) {
    for(int x = 0; x < 13; x++) {
        for(int y = 0; y < 13; y++) {
            // data for this region
        }
    }
}
```

The individual format in each iteration of the loop is:
* 1 bit - set to 0 to indicate to display nothing, 1 to display a region
* 26 bits - if the flag above is set to 1: `region_x << 14 | region_y << 3`

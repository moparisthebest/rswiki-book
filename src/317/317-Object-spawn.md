# Object spawn
This packet requests the client to spawn an object.

## Packet Structure
| Data Type | Description |
|--|--|
| Subtrahend [Byte](/Data-Types.html#common-data-types) | 0 |
| [Little Endian](/Data-Types.html#little-endian) [Byte](/Data-Types.html#common-data-types) | Object ID |
| Subtrahend [Byte](/Data-Types.html#common-data-types) | `object_type << 2 + object_rotation & 3` |

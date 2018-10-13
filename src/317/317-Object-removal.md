# Object removal
This packet requests the client to remove an object.

## Packet Structure
| Data Type | Description |
|--|--|
| Unsigned [Byte](/Data-Types.html#common-data-types) | `object_type << 2 + object_rotation & 3` |
| [Byte](/Data-Types.html#common-data-types) | `0` |

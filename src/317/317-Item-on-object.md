# Item on Object
This packet is sent when a player uses an item on object.

## Packet Details
| Key | Value |
|--|--|
| Name | Item on object |
| Description | Sent when a player uses an item on an objet. |
| Opcode | 192 |
| Type | Fixed |
| Length | 12 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The frame ID. |
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | The object ID. |
| [Big Endian](/Data-Types.html#big-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The objects Y coordinate. |
| [Big Endian](/Data-Types.html#big-endian) [Short](/Data-Types.html#common-data-types) | The items slot ID. |
| [Big Endian](/Data-Types.html#big-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The objects X coordinate. |
| [Short](/Data-Types.html#common-data-types) | The item ID. |

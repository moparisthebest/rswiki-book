# Object action 2
This packet is sent when a player clicks the second option available of an object, such as "Prospect" for rocks.

## Packet Details
| Key | Value |
|--|--|
| Name | Object action 2 |
| Description | Sent when the player clicks the second option available for an an object. |
| Opcode | 252 |
| Type | Fixed |
| Length | 6 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The objects ID. |
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | The objects Y coordinate. |
| [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The objects X coordinate. |

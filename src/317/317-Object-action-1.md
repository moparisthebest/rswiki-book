# Object Action 1
This packet is sent when a player clicks the first option of an object, such as "Cut" for trees or "Mine" for rocks.

## Packet Details
| Key | Value |
|--|--|
| Name | Object action 1 |
| Description | Sent when the player clicks the first option of an object. |
| Opcode | 132 |
| Type | Fixed |
| Length | 6 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The objects X coordinate. |
| [Short](/Data-Types.html#common-data-types) | The objects ID. |
| [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The objects Y coordinate. |

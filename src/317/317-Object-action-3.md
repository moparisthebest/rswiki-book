# Object Action 3
This packet is sent when a player clicks the third action available for an object.

## Packet Details
| Key | Value |
|--|--|
| Name | Object action 3 |
| Description | Sent when a player clicks the third action available for an object. |
| Opcode | 70 |
| Type | Fixed |
| Length | 6 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | The X coordinate of the object. |
| [Short](/Data-Types.html#common-data-types) | The Y coordinate of the object. |
| [Big Endian](/Data-Types.html#big-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The object ID. |

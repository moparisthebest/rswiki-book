# Move Item
This packet is sent when a player moves an item from one slot to another.

## Packet Details
| Key | Value |
|--|--|
| Name | Move item |
| Description | Sent when the player moves an item from one slot to another. |
| Opcode | 214 |
| Type | Fixed |
| Length | 7 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The frame ID. |
| [Byte](/Data-Types.html#common-data-types) | Insert mode. |
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | Starting slot. |
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | New slot. |

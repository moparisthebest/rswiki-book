# Light Item
This packet is sent when a player attempts to light logs on fire.

## Packet Details
| Key | Value |
|--|--|
| Name | Light item |
| Description | Sent when a player attempts to light logs on fire. |
| Opcode | 79 |
| Type | Fixed |
| Length | 6 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Short](/Data-Types.html#common-data-types) | The items Y coordinate. |
| Unsigned [Short](/Data-Types.html#common-data-types) | The item ID. |
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | The items X coordinate. |

# Bank X Items Part-1
This packet is sent when a player requests to bank an X amount of items.

## Packet Details
| Key | Value |
|--|--|
| Name | Bank x items part-1 |
| Description | Sent when a player requests to bank an X amount of items. |
| Opcode | 135 |
| Type | Fixed |
| Length | 6 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | The items slot. |
| Unsigned [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The interface ID. |
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | The item ID. |

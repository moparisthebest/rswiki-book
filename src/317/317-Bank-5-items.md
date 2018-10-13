# Bank 5 Items
This packet is sent when a player attempts to bank 5 of a certain item.

Note: This packet is also used for buying/selling 1 of an item from a shop.

## Packet Details
| Key | Value |
|--|--|
| Name | Bank 5 items |
| Description | Sent when a player attempts to bank 5 of a certain item. |
| Opcode | 117 |
| Type | Fixed |
| Length | 6 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The frame ID. |
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The item ID. |
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | The slot ID. |

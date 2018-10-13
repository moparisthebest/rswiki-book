# Bank 10 Items
This packet is sent when the player attempts to bank 10 of a certain item.

Note: This packet is also used for selling/buying 5 of an item from a shop.

## Packet Details
| Key | Value |
|--|--|
| Name | Bank 10 items |
| Description | Sent when a player banks 10 of a certain item. |
| Opcode | 43 |
| Type | Fixed |
| Length | 6 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | The frame ID. |
| [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The item ID. |
| [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The slot ID. |

# Bank 10 Items
This packet is sent when a player banks all of a certain item they have in their inventory.

Note: This packet is also used for selling/buying 10 items at a shop.

## Packet Details
| Key | Value |
|--|--|
| Name | Bank all items |
| Description | Sent when a player banks all of a certain item they have in their inventory. |
| Opcode | 129 |
| Type | Fixed |
| Length | 6 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| Unsigned [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The items slot ID. |
| Unsigned [Short](/Data-Types.html#common-data-types) | The interface ID. |
| Unsigned [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The item ID. |

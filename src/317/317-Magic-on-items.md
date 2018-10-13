# Magic on Items
This packet is sent when a player casts magic (i.e. High Level Alchemy) on the items in their inventory.

## Packet Details
| Key | Value |
|--|--|
| Name | Magic on items |
| Description | Sent when a player casts magic on the items in their inventory. |
| Opcode | 237 |
| Type | Fixed |
| Length | 8 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Short](/Data-Types.html#common-data-types) | The items slot ID. |
| [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The item ID. |
| [Short](/Data-Types.html#common-data-types) | The frame ID. |
| [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The spell ID. |

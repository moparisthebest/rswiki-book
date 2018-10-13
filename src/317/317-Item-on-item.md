# Item on Item
This packet is sent when a player uses an item on another item.

## Packet Details
| Key | Value |
|--|--|
| Name | Item on item |
| Description | Sent when a player uses an item on another item. |
| Opcode | 53 |
| Type | Fixed |
| Length | 4 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Short](/Data-Types.html#common-data-types) | The item being used on's slot. |
| [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The item being used's slot. |

# Unequip Item
This packet is sent when a player unequips an item.

## Packet Details
| Key | Value |
|--|--|
| Name | Unequip item |
| Description | Sent when a player unequips an item. |
| Opcode | 145 |
| Type | Fixed |
| Length | 6 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| Unsigned [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The interface ID. |
| Unsigned [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The items slot ID. |
| Unsigned [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The item ID. |

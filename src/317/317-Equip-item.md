# Equip Item
This is sent when a player equips an item in-game.

## Packet Details
| Key | Value |
|--|--|
| Name | Equip item |
| Description | Sent when a player equips an item. |
| Opcode | 41 |
| Type | Fixed |
| Length | 6 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| Unsigned [Short](/Data-Types.html#common-data-types) | The ID of the item. |
| Unsigned [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The slot of the item. |
| Unsigned [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The ID of the interface. |

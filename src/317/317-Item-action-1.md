# Item Action 1
This packet is sent when a player clicks the first option of an item, such as "Bury" for bones or "Eat" for food.

## Packet Details
| Key | Value |
|--|--|
| Name | Item action 1 |
| Description | Sent when the player clicks the first option of an item. |
| Opcode | 122 |
| Type | Fixed |
| Length | 6 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The frame ID. |
| [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The slot the item is in. |
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | The ID of the item. |

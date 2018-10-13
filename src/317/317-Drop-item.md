# Drop Item
This packet is sent when a player wants to drop an item onto the ground.

## Packet Details
| Key | Value |
|--|--|
| Name | Drop item |
| Description | Sent when a player wants to drop an item onto the ground. |
| Opcode | 87 |
| Type | Fixed |
| Length | 6 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The item ID. |
| [Short](/Data-Types.html#common-data-types) | The frame ID. |
| [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The slot ID. |

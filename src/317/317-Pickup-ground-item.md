# Pickup Ground Item
This packet is sent when a player clicks the "Pick Up" option on an item when its on the ground.

## Packet Details
| Key | Value |
|--|--|
| Name | Pickup ground item |
| Description | Sent when the player picks up an item from the ground. |
| Opcode | 236 |
| Type | Fixed |
| Length | 6 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | The Y coordinate of the item. |
| [Short](/Data-Types.html#common-data-types) | The item ID. |
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | The X coordinate of the item. |

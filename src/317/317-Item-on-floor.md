# Description
This packet is sent when a player uses an item on another item thats on the floor.

## Packet Details
| Key | Value |
|--|--|
| Name | Item on floor |
| Description | Sent when a player uses an item on another item thats on the floor. |
| Opcode | 25 |
| Type | Fixed |
| Length | 10 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | The interface ID. |
| Unsigned [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The item being used ID. |
| [Short](/Data-Types.html#common-data-types) | The floor items ID. |
| Unsigned [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The Y coordinate of the item. |
| Unsigned [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The items slot ID. |
| [Short](/Data-Types.html#common-data-types) | The X coordinate of the item. |

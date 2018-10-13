# Item on Player
This packet is sent when a player uses an item on another player.

## Packet Details
| Key | Value |
|--|--|
| Name | Item on player |
| Description | Sent when a player uses an item on another player. |
| Opcode | 14 |
| Type | Fixed |
| Length | 8 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The frame ID. |
| [Short](/Data-Types.html#common-data-types) | The other players ID. |
| [Short](/Data-Types.html#common-data-types) | The item ID. |
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | The items slot ID. |

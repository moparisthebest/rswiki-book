# Magic on Player
This packet is sent when the player attempts to cast magic onto another.

## Packet Details
| Key | Value |
|--|--|
| Name | Magic on player |
| Description | This packet is send when a player attempts to cast magic on another |
| Opcode | 249 |
| Type | Fixed |
| Length | 4 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The player index. |
| [Short](/Data-Types.html#common-data-types) [Little Endian](/Data-Types.html#little-endian) | The spell ID. |

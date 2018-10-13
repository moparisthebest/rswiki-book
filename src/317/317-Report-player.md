# Report Player
This packet is sent when a player reports another player.

## Packet Details
| Key | Value |
|--|--|
| Name | Report player |
| Description | Sent when a player reports another player. |
| Opcode | 218 |
| Type | Fixed |
| Length | 8 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Long](/Data-Types.html#common-data-types) | The players name as a long. |
| [Byte](/Data-Types.html#common-data-types) | The rule that's being reported |
| [Byte](/Data-Types.html#common-data-types) | Mute for 48 hours - Sent as either 1 or 0 for a boolean client-side |

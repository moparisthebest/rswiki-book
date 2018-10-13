# Follow
This packet is sent when a player clicks the follow option on another player.

## Packet Details
| Key | Value |
|--|--|
| Name | Follow |
| Description | Sent when a player clicks the follow option on another player |
| Opcode | 39 |
| Type | Fixed |
| Length | 2 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| Unsigned [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | The other players ID. |

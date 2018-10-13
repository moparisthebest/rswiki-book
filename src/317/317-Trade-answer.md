# Trade Answer
This packet is sent when a player answers a trade request from another player.

## Packet Details
| Key | Value |
|--|--|
| Name | Trade answer |
| Description | Sent when a player answers a trade request from another player. |
| Opcode | 139 |
| Type | Fixed |
| Length | 2 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | The player requesting the trade's ID. |

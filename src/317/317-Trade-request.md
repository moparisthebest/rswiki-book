# Trade Request
This packet is sent when a player requests a trade with another player.

## Packet Details
| Key | Value |
|--|--|
| Name | Trade request |
| Description | Sent when a player requests a trade with another player. |
| Opcode | 73 |
| Type | Fixed |
| Length | 2 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | The other players ID. |

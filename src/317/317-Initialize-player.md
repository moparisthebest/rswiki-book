# Initialize Player
Sends the player membership flag and player list index.

## Packet Details
| Key | Value |
|--|--|
| Name | Initialize player |
| Description | Sends the player's membership status and their current index on the server's player list. |
| Opcode | 249 |
| Type | Fixed |
| Length | 3 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Byte](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | Membership flag (1 = member, 0 = free). |
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | Player list index. |

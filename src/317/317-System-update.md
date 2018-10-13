# System Update
A timer showing how many seconds until a 'System Update' will appear in the lower left hand corner of the game screen. After the timer reaches 0 all players are disconnected and are unable to log in again until server is restarted. Players connecting will receive a message stating, "The server is being updated. Please wait 1 minute and try again." (unless stated otherwise).

## Packet Details
| Key | Value |
|--|--|
| Name | System update |
| Description | Sends how many seconds until a 'System Update.' |
| Opcode | 114 |
| Type | Fixed |
| Length | 2 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | Time until an update. |

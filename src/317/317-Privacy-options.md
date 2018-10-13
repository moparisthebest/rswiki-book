# Privacy Options
This packet is sent when a player changes their privacy options (i.e. public chat).

## Packet Details
| Key | Value |
|--|--|
| Name | Privacy options |
| Description | Sent when a player changes their privacy options. |
| Opcode | 95 |
| Type | Fixed |
| Length | 3 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| Unsigned [Byte](/Data-Types.html#common-data-types) | The public chat options. |
| Unsigned [Byte](/Data-Types.html#common-data-types) | The private chat options. |
| Unsigned [Byte](/Data-Types.html#common-data-types) | The trade/compete options. |

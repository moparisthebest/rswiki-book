# Remove Ignore
This packet is sent when a player removes another player from their ignore list.

## Packet Details
| Key | Value |
|--|--|
| Name | Remove ignore |
| Description | Sent when a player removes another player from their ignore list. |
| Opcode | 74 |
| Type | Fixed |
| Length | 8 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Long](/Data-Types.html#common-data-types) | The other players ID. |

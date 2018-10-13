# Add Ignore
This packet is sent when a player adds another player to their ignore list.

## Packet Details
| Key | Value |
|--|--|
| Name | Add ignore |
| Description | Sent when a player adds another player to their ignore list. |
| Opcode | 133 |
| Type | Fixed |
| Length | 8 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Long](/Data-Types.html#common-data-types) | The other players ID. |

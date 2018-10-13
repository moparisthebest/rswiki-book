# NPC Action 1
This packet is sent when a player clicks the first option of an NPC.

## Packet Details
| Key | Value |
|--|--|
| Name | NPC action 1 |
| Description | Sent when a player clicks the first option of an NPC. |
| Opcode | 155 |
| Type | Fixed |
| Length | 2 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | The NPC index. |

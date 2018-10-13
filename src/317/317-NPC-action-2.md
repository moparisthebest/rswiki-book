# NPC Action 2
This packet is sent when a player clicks the second action of an NPC.

## Packet Details
| Key | Value |
|--|--|
| Name | NPC action 2 |
| Description | Sent when a player clicks the second action of an NPC. |
| Opcode | 17 |
| Type | Fixed |
| Length | 2 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The NPC index. |

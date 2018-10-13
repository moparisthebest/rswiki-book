# NPC Action 3
This packet is sent when a player clicks the third option of an NPC.

## Packet Details
| Key | Value |
|--|--|
| Name | NPC action 3 |
| Description | Sent when a player clicks the third option of an NPC. |
| Opcode | 21 |
| Type | Fixed |
| Length | 2 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| Unsigned [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The NPC index. |

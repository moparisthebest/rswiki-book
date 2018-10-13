# Description
This packet is sent when a player attacks an NPC.

## Packet Details
| Key | Value |
|--|--|
| Name | Attack (NPC) |
| Description | Sent when a player attacks an NPC |
| Opcode | 72 |
| Type | Fixed |
| Length | 2 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| Unsigned [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The NPC ID. |

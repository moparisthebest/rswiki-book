# NPC head on interface
Places the head of an NPC on an interface

## Packet Details
| Key | Value |
|--|--|
| Name | NPC head on interface |
| Description | Places the head of an NPC on an interface |
| Opcode | 75 |
| Type | Fixed |
| Length | 4 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The NPC ID |
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The 'slot' ID for where you wish to place the head |

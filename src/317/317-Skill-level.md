# Skill Level
This packet changes the experience and level of a given skill id.

## Packet Details
| Key | Value |
|--|--|
| Name | Skill level |
| Description | Changes the experience and level of a given skill id. |
| Opcode | 134 |
| Type | Fixed |
| Length | 6 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Byte](/Data-Types.html#common-data-types) | The skill ID. |
| [Middle-Endian Small Integer](/Data-Types.html#middle-endian-small-int) | The skill experience. |
| [Byte](/Data-Types.html#common-data-types) | The skill level. |

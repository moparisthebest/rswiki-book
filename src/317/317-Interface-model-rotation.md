# Interface Color
Changes the zoom and rotation of the interface id's media given.

## Packet Details
| Key | Value |
|--|--|
| Name | Interface model rotation |
| Description | Changes the zoom and rotation of the interface id's media given. |
| Opcode | 230 |
| Type | Fixed |
| Length | 8 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The zoom. |
| [Short](/Data-Types.html#common-data-types) | The interface id. |
| [Short](/Data-Types.html#common-data-types) | The rotation1. |
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The rotation2. |

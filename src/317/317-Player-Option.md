# Player Option
Adds an option to a player's right click context menu.

## Packet Details
| Key | Value |
|--|--|
| Name | Player Option |
| Description | Adds an option to a player's right click context menu. |
| Opcode | 104 |
| Type | Variable |
| Length | N/A |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Byte](/Data-Types.html#common-data-types) [Special C](/Data-Types.html#bespoke-data-types) | The option position. |
| [Byte](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | Flag |
| [String](/Data-Types.html#common-data-types) | Action text. |

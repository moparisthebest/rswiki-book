# Send player head model to an interface
This packet sends a players head to an interface

## Packet Details
| Key | Value |
|--|--|
| Name | Send head model to interface. |
| Description | Sends the player head model to an interface. |
| Opcode | 185 |
| Type | Fixed |
| Length | 2 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The interface ID. |

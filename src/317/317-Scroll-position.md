# Scroll Position
This packet sets the scrollbar position of an interface.

## Packet Details
| Key | Value |
|--|--|
| Name | Scroll position |
| Description | Sets the scrollbar position of an interface. |
| Opcode | 79 |
| Type | Fixed |
| Length | 4 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | The interface ID. |
| [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The position of the scrollbar. |

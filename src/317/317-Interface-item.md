# Interface Item
Displays an item model inside an interface.

## Packet Details
| Key | Value |
|--|--|
| Name | Interface item |
| Description | Displays an item model inside an interface. |
| Opcode | 246 |
| Type | Fixed |
| Length | 6 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | Interface ID. |
| [Short](/Data-Types.html#common-data-types) | The item's model zoom. |
| [Short](/Data-Types.html#common-data-types) | The item ID. |

# Clear inventory
Clears a given inventory, by setting all of its item ids to negative one and its item stacks to zero.

## Packet Details
| Key | Value |
|--|--|
| Name | Clear Inventory |
| Description | Used to set all of the items and item stacks in an inventory to nothing. |
| Opcode | 72 |
| Type | Fixed |
| Length | 2 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | The interface ID. |

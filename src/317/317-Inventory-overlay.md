# Child Frame
This packet overlays an interface in the inventory area. This is used in trading and staking.

## Packet Details
| Key | Value |
|--|--|
| Name | Inventory Overlay |
| Description | Overlays an interface on the inventory |
| Opcode | 248 |
| Type | Fixed |
| Length | 4 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The interface to open. |
| [Short](/Data-Types.html#common-data-types) | The interface to overlay the inventory area. |

## Example
`sendFrame248(3323, 3321);`

That will set the open interface to interface 3323, which is the trade interface.
With the inventory overlay interface as 3321, which is an inventory type interface with offer actions.

# Flash sidebar
This packet causes a sidebar icon to start flashing.

## Packet Details
| Key | Value |
|--|--|
| Name | Flash sidebar |
| Description | Causes a sidebar icon to start flashing. |
| Opcode | 24 |
| Type | Fixed |
| Length | 1 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Byte](/Data-Types.html#common-data-types) [Special S](/Data-Types.html#bespoke-data-types) | The sidebar ID. |

## Values
| Sidebar ID | Icon |
|--|--|
| 0 | Attack type |
| -1 | Stats |
| -2 | Quests |
| -3 | Inventory |
| -4 | Wearing |
| -5 | Prayer |
| -6 | Magic |
| -7 | *EMPTY* |
| -8 | Friends list |
| -9 | Ignore list |
| -10 | Log out |
| -11 | Settings |
| -12 | Emotes |
| -13 | Music |

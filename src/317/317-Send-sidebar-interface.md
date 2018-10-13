# Send Sidebar Interface
This packet assigns an interface to one of the tabs in the game sidebar.

## Packet Details
| Key | Value |
|--|--|
| Name | Send sidebar interface |
| Description | Assigns an interface to on of the tabs in the game sidebar. |
| Opcode | 71 |
| Type | Fixed |
| Length | 3 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Short](/Data-Types.html#common-data-types) | The sidebar ID. |
| [Byte](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The interface ID. |

## Values
The below are the different values for this packet.

| Value | Icon | Norm. ID |
|--|--|--|
| 0 | Attack type | 2433 |
| 1 | Stats | 3917 |
| 2 | Quests | 638 |
| 3 | Inventory | 3213 |
| 4 | Wearing | 1644 |
| 5 | Prayer | 5608 |
| 6 | Magic | 1151 |
| 7 | *EMPTY* | N/A |
| 8 | Friends list | 5065 |
| 9 | Ignore list | 5715 |
| 10 | Log out | 2449 |
| 11 | Settings | 4445 |
| 12 | Emotes | 147 |
| 13 | Music | 6299 |

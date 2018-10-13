# Button click
This is sent when a player clicks a button in-game, with the id of the button being clicked.

## Packet Details
| Key | Value |
|--|--|
| Name | Button click |
| Description | Sent when a player clicks an in-game button. |
| Opcode | 185 |
| Type | Fixed |
| Length | 2 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Short](/Data-Types.html#common-data-types) | The button id. |

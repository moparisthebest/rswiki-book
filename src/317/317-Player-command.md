# Player Command
This packet is sent when a player types a message with the prefix '::', the message is then sent to the server and an appropriate action is taken (e.g. spawning an item).

## Packet Details
| Key | Value |
|--|--|
| Name | Player command |
| Description | Sent when a player types a command in the chat box. |
| Opcode | 103 |
| Type | Variable Byte |
| Length | N/A |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [RS String](/RS-String.html) | The command name and parameters. |

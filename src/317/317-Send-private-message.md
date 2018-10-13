# Send Private Message
Sending a private message to another user on the server.

## Packet Details
| Key | Value |
|--|--|
| Name | Sending private message |
| Description | Send Message Sends Message to another user. |
| Opcode | 196 |
| Type | VARIABLE_SHORT |
| Length | N/A |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Long](/Data-Types.html#common-data-types) | Player name. |
| [Int](/Data-Types.html#common-data-types) | Global message counter. |
| [Byte](/Data-Types.html#common-data-types) | Player rights. |

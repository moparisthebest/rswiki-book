# Focus Change
This packet is sent when the game client window goes in and out of focus. The payload consists of one byte that is either 1 or 0; 1 if the client is in focus and 0 if not.

## Packet Details
| Key | Value |
|--|--|
| Name | Focus change |
| Description | Sent when the game client window goes in and out of focus. |
| Opcode | 3 |
| Type | Fixed |
| Length | 1 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Byte](/Data-Types.html#common-data-types) | Whether or not the client is in focus. |

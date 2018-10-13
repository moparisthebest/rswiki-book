# Chat Settings
This packet sends the chat privacy settings.

## Packet Details
| Key | Value |
|--|--|
| Name | Chat settings |
| Description | Sends the chat privacy settings |
| Opcode | 206 |
| Type | Fixed |
| Length | 3 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Byte](/Data-Types.html#common-data-types) | Public chat setting. |
| [Byte](/Data-Types.html#common-data-types) | Private chat setting. |
| [Byte](/Data-Types.html#common-data-types) | Trade setting. |

# Open chatbox interface
Sending this packet to the client will cause the client to open an interface over the chatbox.

## Packet Details
| Key | Value |
|--|--|
| Name | Open chatbox interface |
| Description | Displays an interface over the chatbox. |
| Opcode | 218 |
| Type | Fixed |
| Length | 2 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | Interface ID. |

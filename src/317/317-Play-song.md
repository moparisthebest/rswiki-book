# Play song
Sending this packet to the client will cause the client to start playing a song.

## Packet Details
| Key | Value |
|--|--|
| Name | Play song |
| Description | Starts playing a song. |
| Opcode | 74 |
| Type | Fixed |
| Length | 2 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | The song ID. |

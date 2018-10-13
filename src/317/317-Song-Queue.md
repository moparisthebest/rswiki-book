# Song Queue
This packet queue's a song to be played next.
The client then proceeds to request the queued song using the on-demand protocol.

## Packet Details
| Key | Value |
|--|--|
| Name | Song Queue |
| Description | Queues a song to be played next. |
| Opcode | 121 |
| Type | Fixed |
| Length | 4 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | Song ID |
| [Little Endian](/Data-Types.html#little-endian) [Special A](/Data-Types.html#bespoke-data-types) | Previous Song ID |

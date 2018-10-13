# Audio
Sets what audio to play at a certain moment.

## Packet Details
| Key | Value |
|--|--|
| Name | Audio |
| Description | Sets the audio to play. |
| Opcode | 174 |
| Type | Fixed |
| Length | N/A |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Short](/Data-Types.html#common-data-types) | The sound id. |
| [Byte](/Data-Types.html#common-data-types) | The volume. |
| [Short](/Data-Types.html#common-data-types) | The delay. |

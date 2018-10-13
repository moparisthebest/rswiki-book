# Camera Movement
This packet is sent when a player moves their game camera.

## Packet Details
| Key | Value |
|--|--|
| Name | Camera movement |
| Description | Sent when the player moves the camera. |
| Opcode | 86 |
| Type | Fixed |
| Length | 4 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Short](/Data-Types.html#common-data-types) | The Y coordinate of the camera. |
| [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The X coordinate of the camera. |

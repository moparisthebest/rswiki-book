# Alternate Item Option 2
This packet is sent when a player clicks the alternate second option of an item.

## Packet Details
| Key | Value |
|--|--|
| Name | Alternate Item Option 2 |
| Description | Sent when the player clicks the alternate second option of an item. |
| Opcode | 16 |
| Type | Fixed |
| Length | 6 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The ID of the item. |
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The slot the item is in. |
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The frame ID. |

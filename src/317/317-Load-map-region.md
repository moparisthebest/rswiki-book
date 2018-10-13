# Load Map Region
Makes the client load the specified map region.

## Packet Details
| Key | Value |
|--|--|
| Name | Load map region |
| Description | Makes the client load the specified map region. |
| Opcode | 73 |
| Type | Fixed |
| Length | 4 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | Region X coordinate (absolute X / 8) plus 6. |
| [Short](/Data-Types.html#common-data-types) | Region Y coordinate (absolute Y / 8) plus 6. |

## Other Information
There are various loops/arrays within the map  region loading functionality of the client which have been misunderstood by many.

| Loop type | Description |
|--|--|
| 104 x 104 | Maximum size of the client's load area |
| 8 x 8 | Load blocks to speed up loading NPCs, Items and Objects |
| 13 x 13 | Number of load blocks to load |

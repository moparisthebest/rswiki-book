# Interface Color
This packet changes the color of an interface that is text.

## Packet Details
| Key | Value |
|--|--|
| Name | Interface color |
| Description | This packet changes the color of an interface that is text. |
| Opcode | 122 |
| Type | Fixed |
| Length | 4 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The interface ID. |
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The color. |

##  Information
You use this packet to change the color of text in an interface.

| Color | Code |
|--|--|
| Green | 0x3366 |
| Yellow | 0x33FF66 |
| Red | 0x6000 |

# Force Client Setting
The client stores various user settings in an array, the default values are also stored in another array. This packet changes the default value for a setting and its current value to the one given.

## Packet Details
| Key | Value |
|--|--|
| Name | Force client setting |
| Description | Forcefully alters a client setting value and default value to some supplied value. |
| Opcode | 36 |
| Type | Fixed |
| Length | 3 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Short](/Data-Types.html#common-data-types) [Little Endian](/Data-Types.html#little-endian) | Setting ID number. |
| [Byte](/Data-Types.html#common-data-types) | New value (and default value) for the setting. |

## Other Information
Opcode 87 (length 6) is extremely similar in structure, but the new value is received as an Middle Endian Small Int.
This suggests its for use with bigger setting values.

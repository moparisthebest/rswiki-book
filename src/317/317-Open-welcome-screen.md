# Open Welcome Screen
This packet displays the welcome screen.

## Packet Details
| Key | Value |
|--|--|
| Name | Open welcome screen |
| Description | Displays the welcome screen. |
| Opcode | 176 |
| Type | Fixed |
| Length | 10 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Byte](/Data-Types.html#common-data-types) [Special C](/Data-Types.html#bespoke-data-types) | Days since last recovery change (200 for not yet set, 201 for members server). |
| [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | Number of unread messages. |
| [Byte](/Data-Types.html#common-data-types) | Member warning (1 for member, 0 for non-member). |
| [Middle-Endian Big Integer](/Data-Types.html#middle-endian-big-integer) | Last logged IP. |
| [Short](/Data-Types.html#common-data-types) | Last logged successful log-in. |

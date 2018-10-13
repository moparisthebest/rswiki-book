# Ground Item Action
This packet is sent when a player clicks the first option on a ground item.

## Packet Structure
| Data Type | Description |
|--|--|
| [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | The items X coordinate. |
| Additional [Little Endian](/Data-Types.html#little-endian) [Short](/Data-Types.html#common-data-types) | The items Y coordinate. |
| Additional [Short](/Data-Types.html#common-data-types) | The item ID. |

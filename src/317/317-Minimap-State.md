# Minimap State
This packet sets the Minimaps state, possible values are shown below.

## Packet Details
| Key | Value |
|--|--|
| Name | Minimap State |
| Description | Sets the state of the clients minimap. |
| Opcode | 99 |
| Type | Fixed |
| Length | 1 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Byte](/Data-Types.html#common-data-types) | The state. |

## Values
| State | Description |
|--|--|
| 0 | **Active**: Clickable and viewable |
| 1 | **Locked**: viewable but not clickable |
| 2 | **Blacked-out**: Minimap is replaced with black background |

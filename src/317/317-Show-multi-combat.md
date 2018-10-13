# Show multi-combat
Sending this packet to the client will make the client show the player if they are in a multi-combat zone.

States:

| ID | Name |
|--|--|
| 0 | Not in a multi-combat zone (i.e. no crossbones in bottom-right). |
| 1 | In a multi-combat zone (i.e. crossbones in bottom-right). |

## Packet Details
| Key | Value |
|--|--|
| Name | Show multi-combat |
| Description | Shows the player if they are in a multi-combat zone. |
| Opcode | 61 |
| Type | Fixed |
| Length | 1 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Byte](/Data-Types.html#common-data-types) | The state. |

# Set Interface Text
Sets the text for the specific interface.

## Packet Details
| Key | Value |
|--|--|
| Name | Set interface text |
| Description | Sets the text for a specified interface |
| Opcode | 126 |
| Type | VARIABLE_SHORT |
| Length | N/A |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [RS String](/RS-String.html) | The new text for the interface |
| [Short](/Data-Types.html#common-data-types) [Special A](/Data-Types.html#bespoke-data-types) | The interface id |

## Information
I do not recommend you use this to change the text color.
I refer you to [Interface Color](317-Interface-color.html) packet for the proper way to do so.

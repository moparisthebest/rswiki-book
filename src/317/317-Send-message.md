# Send Message
Sends a server side message (e.g. 'Welcome to RuneScape'), or a trade/duel/challenge request. 

The format for sending such requests is: `[player name][request type]`.
Where `[request type]` is one of `:duelreq:`, `:chalreq:`, or `:tradereq:`.

Example: Trading a player called 'mopar': `mopar:tradereq:`.

## Packet Details
| Key | Value |
|--|--|
| Name | Send message |
| Description | Sends a server message, trade or duel request to the client's chat panel. |
| Opcode | 253 |
| Type | Variable Byte |
| Length | N/A |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [RS String](/RS-String.html) | The message. |

\[\[Category Packet\]\] \[\[Category Packet 317\]\] {{packet\|name=Send
message\|description=Sends a server message, trade or duel request to
the client's chat panel.\|opcode=253\|type=Variable
Byte\|length=N/A\|revision=317}} == Send Message ==

=== Description ===

Sends a server side message (e.g. 'Welcome to RuneScape'), or
trade/duel/challenge request.

The format for sending such requests is: '\[player name\]\[request
type\]'. Where request type can be one of the following: ':duelreq:',
':chalreq:' or ':tradereq:'. An example for trading the player 'mopar'
would be: 'mopar:tradereq:'.

=== Packet Structure ===

{\| border=2 ! Data type ! Description \|- \| \[\[RS String\|RS
String\]\] \| The message. \|- \|}

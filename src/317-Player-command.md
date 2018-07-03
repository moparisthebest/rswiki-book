\[\[Category Packet\]\] \[\[Category Packet 317\]\]
{{packet\|name=Player command\|description=Sent when a player types a
command in the chat box.\|opcode=103\|type=Variable
Byte\|length=N/A\|revision=317}} == Player Command ==

=== Description ===

This packet is sent when a player types a message with the prefix '::',
the message is then sent to the server and an appropriate action is
taken (e.g. spawning an item).

=== Packet Structure === {\|border=2 ! Data Type ! Description \|- \|
\[\[RS String\|RS String\]\] \| The command name and parameters. \|}

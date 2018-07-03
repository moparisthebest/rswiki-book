\[\[Category Packet\]\] \[\[Category Packet 317\]\] {{packet\|name=Focus
change\|description=Sent when the game client window goes in and out of
focus.\|opcode=3\|type=Fixed\|length=1\|revision=317}} == Focus Change
==

=== Description ===

This packet is sent when the game client window goes in and out of
focus. The payload consists of one byte that is either 1 or 0; 1 if the
client is in focus and 0 if not.

=== Packet Structure === {\|border=2 ! Data Type ! Description \|- \|
\[\[Data Types\#Standard data types\|Byte\]\] \| Whether or not the
client is in focus. \|- \|}

\[\[Category Packet\]\] \[\[Category Packet 317\]\]
{{packet\|name=Privacy options\|description=Sent when a player changes
their privacy options.\|opcode=95\|type=Fixed\|length=3\|revision=317}}
== Privacy Options ==

=== Description ===

This packet is sent when a player changes their privacy options
(i.e. public chat).

=== Packet Structure === {\|border=2 ! Data Type ! Description \|- \|
Unsigned \[\[Data Types\#Standard data types\|Byte\]\] \| The public
chat options. \|- \| Unsigned \[\[Data Types\#Standard data
types\|Byte\]\] \| The private chat options. \|- \| Unsigned \[\[Data
Types\#Standard data types\|Byte\]\] \| The trade/compete options. \|-
\|}

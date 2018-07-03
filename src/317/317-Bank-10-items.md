\[\[Category Packet\]\] \[\[Category Packet 317\]\] {{packet\|name=Bank
10 items\|description=Sent when a player banks 10 of a certain
item.\|opcode=43\|type=Fixed\|length=6\|revision=317}} == Bank 10 Items
==

=== Description ===

This packet is sent when the player attempts to bank 10 of a certain
item.<br> '''Note:''' This packet is also used for selling/buying 5 of
an item from a shop.

=== Packet Structure === {\|border=2 ! Data Type ! Description \|- \|
\[\[Data Types\#Little Endian\|Little Endian\]\] \[\[Data
Types\#Standard data types\|Short\]\] \| The frame ID. \|- \| \[\[Data
Types\#Standard data types\|Short\]\] \[\[Data Types\#Non Standard Data
Types\|Special A\]\] \| The item ID. \|- \| \[\[Data Types\#Standard
data types\|Short\]\] \[\[Data Types\#Non Standard Data Types\|Special
A\]\] \| The slot ID. \|}

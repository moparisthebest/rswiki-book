\[\[Category Packet\]\] \[\[Category Packet 317\]\]
{{packet\|name=Initialize player\|description=Sends the player's
membership status and their current index on the server's player
list.\|opcode=249\|type=Fixed\|length=3\|revision=317}} == Initialize
Player ==

=== Description ===

Sends the player membership flag and player list index.

=== Packet Structure ===

{\| border=2 ! Data type ! Description \|- \| \[\[Data Types\#Standard
data types\|Byte\]\] \[\[Data Types\#Non Standard Data Types\|Special
A\]\] \| Membership flag (1 = member, 0 = free). \|- \| \[\[Data
Types\#Little Endian\|Little Endian\]\] \[\[Data Types\#Standard data
types\|Short\]\] \[\[Data Types\#Non Standard Data Types\|Special A\]\]
\| Player list index. \|- \|}

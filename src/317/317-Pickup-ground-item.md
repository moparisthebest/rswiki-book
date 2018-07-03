\[\[Category Packet\]\] \[\[Category Packet 317\]\]
{{packet\|name=Pickup ground item\|description=Sent when the player
picks up an item from the
ground.\|opcode=236\|type=Fixed\|length=6\|revision=317}} == Pickup
Ground Item ==

=== Description ===

This packet is sent when a player clicks the "Pick Up" option on an item
when its on the ground.

=== Packet Structure === {\|border=2 ! Data Type ! Description \|- \|
\[\[Data Types\#Little Endian\|Little Endian\]\] \[\[Data
Types\#Standard data types\|Short\]\] \| The Y coordinate of the item.
\|- \| \[\[Data Types\#Standard data types\|Short\]\] \| The item ID.
\|- \| \[\[Data Types\#Little Endian\|Little Endian\]\] \[\[Data
Types\#Standard data types\|Short\]\] \| The X coordinate of the item.
\|- \|}

\[\[Category Packet\]\] \[\[Category Packet 317\]\] {{packet\|name=Clear
Inventory\|description=Used to set all of the items and item stacks in
an inventory to
nothing.\|opcode=72\|type=Fixed\|length=2\|revision=317}} == Clear
inventory ==

=== Description ===

This packet creates a loop through a given inventory interface id and
sets the item ids to negative one and the item stacks to zero.

=== Packet Structure === {\|border=2 ! Data Type ! Description \|- \|
\[\[Data Types\#Little Endian\|Little Endian\]\] \[\[Data
Types\#Standard data types\|Short\]\] \| The interface ID. \|- \|}

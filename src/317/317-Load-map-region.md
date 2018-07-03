\[\[Category Packet\]\] \[\[Category Packet 317\]\] {{packet\|name=Load
map region\|description=Makes the client load the specified map
region.\|opcode=73\|type=Fixed\|length=4\|revision=317}} == Load Map
Region ==

=== Description ===

Makes the client load the specified map region.

=== Packet Structure ===

{\| border=2 ! Data type ! Description \|- \| \[\[Data Types\#Standard
data types\|Short\]\] \[\[Data Types\#Non Standard Data Types\|Special
A\]\] \| Region X coordinate (absolute X / 8) plus 6. \|- \| \[\[Data
Types\#Standard data types\|Short\]\] \| Region Y coordinate (absolute Y
/ 8) plus 6. \|- \|}

=== Other Information === There are various loops/arrays within the map
region loading functionality of the client which have been misunderstood
by many. {\| border=2 ! Loop type ! Description \|- \| 104 x 104 \|
Maximum size of the client's load area \|- \| 8 x 8 \| Load blocks to
speed up loading NPCs, Items and Objects \|- \| 13 x 13 \| Number of
load blocks to load \|- \|}

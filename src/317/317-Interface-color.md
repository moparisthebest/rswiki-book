\[\[Category Packet\]\] \[\[Category Packet 317\]\]
{{packet\|name=Interface color\|description=This packet changes the
color of an interface that is
text.\|opcode=122\|type=Fixed\|length=4\|revision=317}} == Interface
Color ==

=== Description ===

This packet changes the color of an interface that is text.

=== Packet Structure === {\|border=2 ! Data Type ! Description \|- \|
\[\[Data Types\#Little Endian\|Little Endian\]\] \[\[Data
Types\#Standard data types\|Short\]\] \[\[Data Types\#Non Standard Data
Types\|Special A\]\] \| The interface ID. \|- \| \[\[Data Types\#Little
Endian\|Little Endian\]\] \[\[Data Types\#Standard data types\|Short\]\]
\[\[Data Types\#Non Standard Data Types\|Special A\]\] \| The color. \|-
\|}

=== Information === You use this packet to change the color of text in
an interface.

{\|border=2 ! Color ! Code \|- \| Green \| 0x3366 \|- \| Yellow \|
0x33FF66 \|- \| Red \| 0x6000 \|- \|}

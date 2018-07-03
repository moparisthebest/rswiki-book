\[\[Category Packet\]\] \[\[Category Packet 317\]\]
{{packet\|name=Update item container\|description=Updates items in an
interface
component.\|opcode=53\|type=VARIABLE\_SHORT\|length=N/A\|revision=317}}
== Update item container ==

=== Description === Updates the items in a given interface component.

=== Packet Structure ===

{\| border=2 ! Data type ! Description \|- \| Unsigned \[\[Data
Types\#Standard data types\|Short\]\] \| Interface ID. \|- \| Unsigned
\[\[Data Types\#Standard data types\|Short\]\] \| Amount of items. \|-
\|}

The rest in pseudo-code:

for (i = 0; i \< amt\_of\_items; i++) { item\_amount = read\_u\_byte();
// Item Amount: U Byte

if (item\_amount == 255) item\_amount = read\_int\_me\_b(); // Item
Amount (if entered as 255 previously - to allow bigger amounts than
254): Integer Middle-Endian Big (Inverse middle)

item\_id = read\_u\_short\_le\_a(); // Item ID: U Short Little Endian
Special A }

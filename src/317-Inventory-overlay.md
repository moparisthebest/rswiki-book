\[\[Category Packet\]\] \[\[Category Packet 317\]\]
{{packet\|name=Inventory Overlay\|description=Overlays an interface on
the inventory\|opcode=248\|type=Fixed\|length=4\|revision=317}} == Child
Frame ==

=== Description ===

This packet overlays an interface in the inventory area. This is used in
trading and staking.

=== Example ===

<pre>sendFrame248(3323, 3321);</pre>
That will set the open interface to interface 3323, which is the trade
interface, with the inventory overlay interface as 3321, which is an
inventory type interface with offer actions.

=== Packet Structure === {\|border=2 ! Data Type ! Description \|- \|
\[\[Data Types\#Standard data types\|Short\]\] \[\[Data Types\#Non
Standard data types\|Special A\]\] \| The interface to open. \|- \|
\[\[Data Types\#Standard data types\|Short\]\] \| The interface to
overlay the inventory area. \|- \|}

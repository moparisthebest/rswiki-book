\[\[Category Packet\]\] \[\[Category Packet 317\]\] {{packet\|name=Show
multi-combat\|description=Shows the player if they are in a multi-combat
zone.\|opcode=61\|type=Fixed\|length=1\|revision=317}} == Show
multi-combat ==

=== Description ===

Sending this packet to the client will make the client show the player
if they are in a multi-combat zone.

'''States:''' \* 0 - Not in a multi-combat zone, no crossbones in
bottom-right. \* 1 - In a multi-combat zone, crossbones in bottom-right.

=== Packet Structure === {\|border=2 ! Data Type ! Description \|- \|
\[\[Data Types\#byte\|byte\]\] \| The state. \|- \|}

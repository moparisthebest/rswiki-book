\[\[Category Packet\]\] \[\[Category Packet 317\]\]
{{packet\|name=Display hint icon\|description=Display a hint icon to the
player.\|opcode=254\|type=Variable Byte\|length=N/A\|revision=317}}

== Display Hint Icon ==

=== Description ===

Displays a hint icon.

=== Packet Structure ===

{\| border=2 ! Data type ! Description \|- \| \[\[Data Types\#Standard
data types\|Byte\]\] \| The Icon type \|- \|}

=== if type == 1 ===

{\| border=2 ! Data type ! Description \|- \| \[\[Data Types\#Standard
data type\|Short\]\] \| Icon NPC target \|- \|}

=== if type \>= 2 && type \<= 6 ===

{\| border=2 ! Data type ! Description \|- \| \[\[Data Types\#Standard
data type\|Short\]\] \| Icon X \|- \| \[\[Data Types\#Standard data
type\|Short\]\] \| Icon Y \|- \| \[\[Data Types\#Standard data
types\|Byte\]\] \| Icon draw height \|- \|}

=== if type == 10 ===

{\| border=2 ! Data type ! Description \|- \| \[\[Data Types\#Standard
data type\|Short\]\] \| Icon player target \|- \|}

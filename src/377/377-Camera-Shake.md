\[\[Category Packet\]\] \[\[Category Packet 377\]\]
{{packet\|name=Camera Shake\|description=Set camera shake
parameters.\|opcode=67\|type=Fixed\|length=4\|revision=377}} == Camera
Shake ==

=== Description === Set camera shake parameters. It may be worth reading
about Sine Waves \[http://en.wikipedia.org/wiki/Sine\_wave\].

=== Packet Structure ===

{\| border=2 ! Data type ! Description \|- \| \[\[Data Types\#Standard
data types\|Byte\]\] \| The index of the shake parameter to modify. \|-
\| \[\[Data Types\#Standard data types\|Byte\]\] \| The range of the
shake randomness. \|- \| \[\[Data Types\#Standard data types\|Byte\]\]
\| The amplitude (maximum displacement from 0) of the shake. \|- \|
\[\[Data Types\#Standard data types\|Byte\]\] \| The phase (where in its
cycle the oscillation is at t = 0) of the shake. \|- \|}

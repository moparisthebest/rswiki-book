\[\[Category RS2\]\] == '''Login Protocol''' ==

The Login protocol is identical to the \[\[317 Protocol\#Login Protocol
Overview\|317 Login protocol\]\].

== Game Protocol ==

=== Server -\> Client Packets === {\| border=2 \|- ! Opcode ! Type !
Length (bytes) ! Name ! Description \|- ! 31 ! VARIABLE\_BYTE ! N/A !
\[\[357 Send Message\|Send Message\]\] ! Sends a message to the client,
such as 'Welcome to RuneScape'. \|- ! 96 ! VARIBLE\_BYTE ! N/A ! \[\[357
Send Inventory\|Send Inventory\]\] ! Sends the players inventory to the
client. \|- ! 121 ! FIXED ! 4 ! \[\[357 Load Map Region\|Load Map
Region\]\] ! Tells the client to load a map region depending on the
region's X and Y coordinates. \|- ! 163 ! FIXED ! 3 ! \[\[357 Send
Sidebar Interface\|Send Sidebar Interface\]\] ! Assigns an interface to
one of the tabs in the game sidebar. \|-}

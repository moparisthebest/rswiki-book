\[\[Category Packet\]\] \[\[Category Packet 194\]\] \[\[Category RS2\]\]

Just in case somebody cares about this.

== '''Packet structure''' == ?

== '''Login''' == ?

== '''Game Protocol''' ==

===Server -\> Client Packets===

  {
  ---

! Opcode ! Type ! Length (bytes) ! Name ! Description \|- \| 137 \|
FIXED \| 2 \| \[\[194 Show interface\|Show interface\]\] \| Displays a
normal interface. \|- \| 164 \| VARIABLE\_BYTE \| N/A \| \[\[194 Send
message\|Send message\]\] \| Sends a server message (e.g. 'Welcome to
RuneScape') or trade/duel request. \|- \| 192 \| FIXED \| 0 \| \[\[194
Logout\|Logout\]\] \| Disconnects the client from the server. \|- \| 206
\| VARIABLE\_BYTE \| N/A \| \[\[194 Set MIDI\|Set MIDI\]\] \| Sets the
current song playing on the client. \|- \| 210 \| FIXED \| 3 \| \[\[194
Send sidebar interface\|Send sidebar interface\]\] \| Assigns an
interface to one of the tabs in the game sidebar. \|- \| 240 \| FIXED \|
0 \| \[\[194 Clear screen\|Clear screen\]\] \| Clears the screen of all
open interfaces. \|- \|}

===Client -\> Server Packets===

  {
  ---

! Opcode ! Type ! Length (bytes) ! Name ! Description \|- \| 54 \|
VARIABLE\_BYTE \| N/A \| Send Chat Message \| Sends a chat message to
the server. \|- \| 237 \| VARIABLE\_BYTE \| N/A \| Send Command \| Sends
a command (any message prefixed with ::) to the server. \|- \|}

\[\[Category Packet\]\] \[\[Category Packet 377\]\] \[\[Category RS2\]\]

== '''Login Protocol''' ==

The Login protocol is identical to the \[\[317 Protocol\#Login Protocol
Overview\|317 Login protocol\]\].

==Game Protocol== The game protocol is the in-game communication of
player actions between the server and client. <br/>

===Server -\> Client Packets===

  {
  ---

! Opcode ! Type ! Length (bytes) ! Name ! Description \|- ! 2 ! FIXED !
4 ! \[\[377 Interface Animation\|Interface Animation\]\] ! Sets an
interface's model animation. \|- ! 3 ! FIXED ! 6 ! \[\[377 Move
Camera\|Camera Move\]\] ! Moves the camera. \|- ! 5 ! FIXED ! 0 !
\[\[377 Logout\|Logout\]\] ! Disconnects the client from the server. \|-
! 10 ! FIXED ! 3 ! \[\[377 Send Sidebar Interface\|Send Sidebar
Interface\]\] ! Assigns an interface to one of the tabs in the game
sidebar. \|- ! 13 ! FIXED ! 0 ! \[\[377 Animation Reset\|Animation
Reset\]\] ! Resets all entity animations in the immediate area. \|- ! 18
! FIXED ! 6 ! \[\[377 Interface Model Rotation\|Interface Model
Rotation\]\] ! Sets the rotation speed of an item in an interface. \|- !
21 ! FIXED ! 6 ! \[\[377 Interface Item\|Interface Item\]\] ! Displays
an item model inside an interface. \|- ! 26 ! FIXED ! 5 ! \[\[377 Send
Sound\|Send Sound\]\] ! Sends a sound to be played. \|- ! 29 ! FIXED ! 0
! \[\[377 Reset Open Interfaces\|Reset Open Interfaces\]\] ! Resets all
opened interfaces. \|- ! 40 ! FIXED ! 2 ! \[\[377 Reset Ground Items and
Objects\|Reset Ground Items and Objects\]\] ! Resets all ground items
and objects in a 8x8 region. \|- \|- ! 41 ! FIXED ! 4 ! \[\[377 Play
Ambient Wave\|Play Ambient Wave\]\] ! Plays an ambient wave. \|- ! 49 !
FIXED ! 6 ! \[\[377 Skill Level\|Skill Level\]\] ! Sends a skill level
to the client. \|- ! 50 ! FIXED ! 2 ! \[\[377 Walkable
Interface\|Walkable Interface\]\] ! Displays an interface in walkable
mode. \|- ! 53 ! VARIABLE\_SHORT ! N/A ! \[\[377 Construct Map
Region\|Construct Map Region\]\] ! Constructs a map region given the
region's x and y coordinate. \|- ! 58 ! FIXED ! 0 ! \[\[377 Input
Amount\|Input Amount\]\] ! Displays the "Input amount" interface. \|- !
59 ! FIXED ! 6 ! \[\[377 Create Static Graphic\|Create Static
Graphic\]\] ! Creates a static graphic. \|- ! 61 ! FIXED ! 0 ! \[\[377
Clear Waypoint\|Clear Waypoint\]\] ! Resets the waypoint. \|- ! 63 !
VARIABLE\_BYTE ! N/A ! \[\[377 Send Message\|Send Message\]\] ! Sends a
server message (e.g. 'Welcome to RuneScape') or trade/duel request. \|-
! 67 ! FIXED ! 4 ! \[\[377 Camera Shake\|Camera Shake\]\] ! Causes the
camera to shake. \|- ! 71 ! VARIABLE\_SHORT ! N/A ! \[\[377 Update
Npcs\|Update Npcs\]\] ! Updates NPCs. \|- ! 75 ! FIXED ! 2 ! \[\[377
Send Position\|Send Position\]\] ! Sends a position (used for packets
such as Ground Items and Projectiles) \|- ! 76 ! FIXED ! 23 ! \[\[377
Open Welcome Screen\|Open Welcome Screen\]\] ! Displays the welcome
screen. \|- ! 78 ! FIXED ! 9 ! \[\[377 Send Add Friend\|Send Add
Friend\]\] ! Sends a friend to be added to the friend list. \|- ! 82 !
FIXED ! 3 ! \[\[377 Set Widget Mouse Triggered\|Set Widget Mouse
Triggered\]\] ! Set widget mouse triggered. \|- ! 88 ! FIXED ! 2 !
\[\[377 Create Object\|Create Object\]\] ! Sends a friend to be added to
the friend list. \|- ! 90 ! VARIABLE\_SHORT ! N/A ! \[\[377 Update
Players\|Update Players\]\] ! Updates players. \|- ! 107 ! FIXED ! 5 !
\[\[377 Send Ground Item\|Send Ground Item\]\] ! Adds a ground item to
the server. \|- ! 113 ! FIXED ! 0 ! \[\[377 Reset Button State\|Reset
Button State\]\] ! Resets the button state for all buttons. \|- ! 125 !
FIXED ! 1 ! \[\[377 Run Energy\|Run Energy\]\] ! Sends the players run
energy level. \|- ! 126 ! FIXED ! 3 ! \[\[377 Initialize
Player\|Initialize Player\]\] ! Sends the player's membership status and
their current index on the server's player list. \|- ! 128 ! FIXED ! 4 !
\[\[377 Inventory Overlay\|Inventory Overlay\]\] ! Displays an interface
over the sidebar area. \|-}

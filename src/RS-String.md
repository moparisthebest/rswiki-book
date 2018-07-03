# RS String

RS String is the internal name for a custom string data-type used in the
RuneScape protocol.
The string data-type stores a collection of characters in order to
represent a textual message.

## Old Engine

In the old engine client, the RS String datatype is terminated by the new line
character (i.e. `\n`).

# New Engine

In the new-engine client, the RS String datatype is terminated by a null byte (i.e. `0`).

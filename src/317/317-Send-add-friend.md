# Send Add Friend
Sends friend data to the client

Attempts to update player node, if player isn't in the friends list and there is space, the player is added to the friend list.

## Packet Structure
| Data type | Description |
|--|--|
| [Long](/Data-Types.html#common-data-types) | Player name |
| [Byte](/Data-Types.html#common-data-types) | The world (10 = "online" in world 1, 0 = logged out) |

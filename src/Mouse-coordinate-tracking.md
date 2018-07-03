# Mouse coordinate tracking

There is a mechanicsm of mouse coordinate tracking within the client.
This records the `(x, y)` coordinates of the mouse, and sends them
back to the server each tick.

When the client connects with the server, after it receives
the player privilege, it receives a byte denoting whether or not
the client should send these coordinates to the server periodically.

## Packet structure
```
byte opcode = 45;
byte dummy = 0;
byte[] mouse_data;
```

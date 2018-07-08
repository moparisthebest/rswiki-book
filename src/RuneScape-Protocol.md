# RuneScape Protocol

The RuneScape Protocol is the protocol used for data transmission
between the RuneScape client and server.
The protocol changes with every revision, however, typically only the packet
opcodes are changed, and possibly some new packets are added.

The entire protocol is generally separated into two sub-protocols:

* Login Protocol
* Game Protocol

## Login Protocol

The Login Protocol is the protocol that is used to log a player into
RuneScape. This protocol contains information that sets up the
encryption for the entire session, using the ISAAC algorithm. The "login
block" is encrypted using RSA to prevent third party programs from
packet-sniffing the ISAAC cipher keys and breaking the session
encryption for the purpose of monitoring, injecting, and generally
sniffing packets.

## Game Protocol

The Game Protocol is the protocol in which game action information is
transmitted. The opcodes are encrypted using ISAAC in order to prevent
third party programs from tampering with the stream. The game protocol
is made up of packets that are structured like so:

```
for fixed-size packets:
    opcode, payload[size]

for variable-sized packets:
    opcode, size, payload[size]
```

The `opcode` of a game packet is basically an identifier for the type
of game action that the packet represents. The `size` of the packet is
the amount of bytes that the payload of the packet carries, and the
`payload` is an array of bytes that holds the actual data
(information) of the packet.

A `fixed-size` packet is a packet whose payload size does never
change, and the size for the specified opcode is already known between
both client and server. A `variable-sized` packet is a packet whose
payload size changes according to the situation of the game session.

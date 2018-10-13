# Send ignored users
Sends the IDs of all the users that this player has in their ignore.

Note: By looking at the rest of the 317 protocol, there doesn't seem to be a way to change the list dynamically.
It seems as though that whenever the player decides to add or remove a player from their list, it must send all the values again.

## Packet Details
| Key | Value |
|--|--|
| Name | Send ignored users |
| Description | Sends a list of all the ignored player IDs |
| Opcode | 214 |
| Type | VARIABLE_SHORT |
| Length | N/A |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| Long block (see blow) | Player name |

## Long block
This packet has a slightly different structure than the other packets.

```java
int entries = packetSize / 8;

for (int i = 0; i < entries; i++) {
    ignoreList[i] = stream.readLong();
}
```

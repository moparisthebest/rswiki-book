\[\[Category Packet\]\] \[\[Category Packet 317\]\]
<h3>
[ Description ]{.mw-headline}
</h3>
<p>
Sends friend data to the client

Attempts to update player node, if player isn't in the friends list and
there is space, the player is added to the friend list.
</p>
<h3>
[ Packet Structure ]{.mw-headline}
</h3>
<table border="2">
<tr>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
<tr>
<td>
Long
</td>
<td>
The player name
</td>
</tr>
<td>
Byte
</td>
<td>
The world (10 = "online" for most clients, 0 = logged out)
</td>
</table>

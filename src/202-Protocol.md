\[\[Category RSC\]\]

This page refers to the RSC \#202 client revision (the original
distribution by eXemplar)

== '''Packet structure''' == ?

== '''Login''' == ?

== '''Incoming Data''' == '''TODO:''' Document packet structures
<pre>
#define IDX_WEIRD_USERNAME    32
#define IDX_LOGIN             0
#define IDO_LOGOUT_ACK        39                    // acknowledge logout command from server
#define IDO_PING              153                   // send ping to server, so it knows we're still there
#define IDO_IGNORE_ADD        25                    // add name to ignore list
#define IDO_IGNORE_REMOVE     108                   // remove name from ignore list
#define IDO_FRIENDS_ADD       168                   // add name to friends list
#define IDO_FRIENDS_REMOVE    52                    // remove name from friends list
#define IDO_PM_FRIEND         254                   // send pm to someone in friends list
#define IDO_SEND_CHAT         145
#define IDO_SEND_SERVER_CMD   90                    // sends a command to the server (type "::xxx" in chat and it sends command 'xxx')
#define IDO_UPDATE_SETTINGS   176                   // changes settings (chatblock, privateblock, tradeblock, duelblock)

#define IDO_LOGOUT            129
#define IDO_CHAR_DESIGN       218                   // send character design (makeover mage, creation)
#define IDO_SLEEPWORD         72
#define IDO_NEW_PLAYER_ACK    83                    // send ids of newly added player back to server, if it wants to

#define IDO_EXCEPTION_SEND    156
#define IDO_WALKCMD_1         246
#define IDO_WALKCMD_2         132
#define IDO_CLICKDIALOGITEM   154
#define IDO_SETCOMBATSTYLE    41
#define IDO_WITHDRAW          183
#define IDO_DEPOSIT           198
#define IDO_CLOSE_BANK        48
#define IDO_BUYITEM           128
#define IDO_SELLITEM          255
#define IDO_CLOSE_SHOP        253
#define IDO_CANCEL_TRADE      216
#define IDO_CONFIRM_TRADE     53
#define IDO_TRADE_UPDATE      70
#define IDO_ACCEPT_TRADE      211
#define IDO_DUEL_CONFIRM_1    87
#define IDO_DUEL_UPDATE       123
#define IDO_DUEL_FLAG_1       225
#define IDO_DUEL_FLAG_2       252
#define IDO_CANCEL_DUEL       35
#define IDO_PRAYER_OFF        248
#define IDO_PRAYER_ON         56
#define IDO_CHANGE_SETTINGS   157

// action commands...
#define IDO_CAST_GR_ITEM      104
#define IDO_USEWITH_GR_ITEM   34
#define IDO_TAKE_ITEM         245
#define IDO_CAST_WALLOBJ      67
#define IDO_USEWITH_WALLOBJ   36
#define IDO_WALLOBJ_CMD1      126
#define IDO_WALLOBJ_CMD2      235
#define IDO_CAST_OBJECT       17
#define IDO_USEWITH_OBJECT    94
#define IDO_OBJECT_CMD1       51
#define IDO_OBJECT_CMD2       40

#define IDO_CAST_INVITEM      49
#define IDO_USEWITH_INVITEM   27
#define IDO_REMOVE_ITEM       92
#define IDO_WEAR_ITEM         181
#define IDO_INVITEM_CMD       89
#define IDO_DROP_ITEM         147

#define IDO_CAST_NPC          71
#define IDO_USEWITH_NPC       142
#define IDO_TALK_NPC          177
#define IDO_NPC_CMD           74
#define IDO_ATTACK_NPC        73

#define IDO_CAST_PLAYER       55
#define IDO_USEWITH_PLAYER    16
#define IDO_ATTACK_PLAYER     57
#define IDO_DUEL_PLAYER       222
#define IDO_TRADE_PLAYER      166
#define IDO_FOLLOW_PLAYER     68

#define IDO_CAST_GROUND       232
#define IDO_CAST_SELF         206

#define IDO_REPORT_ABUSE      7
</pre>
<table border="1" cellpadding="3" cellspacing="3">
<tr>
<td>
<b>opcode</b>
</td>
<td>
<b>usage</b>
</td>
<td>
<b>size</b>
</td>
<td>
<b>payload</b>
</td>
</tr>
<tr>
<td>
</td>
<td>
</td>
<td>
</td>
<td>
</td>
</tr>
</table>
== '''Outgoing Data''' == '''TODO:''' Document packet structures
<pre>
// login responses...
#define IDX_MOD_ACCEPTED      25                    // logged in as player mod
#define IDX_LOGIN_SUCCESS     0
#define IDX_RELOGIN_SUCCESS   1                     // connection reestablished after lost connection...
#define IDX_WRONG_PWD         3
#define IDX_NAME_LOGGED_IN    4
#define IDX_CLIENT_UPDATED    5
#define IDX_IP_IN_USE         6
#define IDX_LOGINS_EXCEEDED   7
#define IDX_SERV_REJECTED     8
#define IDX_LOGINSERV_REJCT   9
#define IDX_NAME_IN_USE       10
#define IDX_TEMP_DISABLED     11
#define IDX_PERM_DISABLED     12
#define IDX_SERVER_FULL       14
#define IDX_MEMBERACC_REQ     15                    // requires member account to login here
#define IDX_LOGINSERV_DOWN    16
#define IDX_DECODE_FAIL       17
#define IDX_LOGIN_MISMATCH    20

#define IDI_MESSAGE           48                    // (game) messages from server
#define IDI_LOGOUT            222                   // logout command from server (forced, or initiated by client IDO_LOGOUT)
#define IDI_LOGOUT_REJECT     136                   // not allowed to log out (e.g. when in combat)
#define IDI_FRIENDS_LOAD      249                   // when logging in, sends the whole friends list to the client
#define IDI_FRIEND_LOGGED     25                    // a friend from friends list logged in or out (also used to add a friend to friends list)
#define IDI_IGNORE_LOAD       2                     // when logging in, sends the whole ignore list to the client
#define IDI_SETTINGS_LOAD     158                   // load settings upon logging in (blocks)
#define IDI_FRIENDS_PM        170                   // someone pm'd us

#define IDI_PLAYER_MOVEMENT   145                   // player movement update
#define IDI_GRITEMS_UPDATE    109                   // update ground items
#define IDI_OBJECTS_UPDATE    27
#define IDI_INV_LOAD          114                   // load inventory
#define IDI_PLAYER_UPDATE     53
#define IDI_WALLOBJ_UPDATE    95
#define IDI_NPC_MOVEMENT      77                    // npc movement update
#define IDI_NPC_UPDATE        190
#define IDI_DIALOG_SHOW       223
#define IDI_DIALOG_CLOSE      127
#define IDI_LOAD_NEWMAPAREA   131                   // entering a new region (maparea)
#define IDI_XP_LOAD           180                   // load xp and stats
#define IDI_EQUIP_UPDATE      177                   // equipment stats (armour, magic, prayer, weapaim/power)
#define IDI_PLAYER_DIED       165
#define IDI_LOADWORLD         115                   // load objects, wallobjects, items
#define IDI_DESIGN_CHAR       207
#define IDI_OPEN_TRADE_1      4
#define IDI_CLOSE_TRADE       187
#define IDI_TRADE_UPDATE      250                   // opponents offer was updated
#define IDI_TRADE_B_UPDATE    92                    // update of opponents acception status
#define IDI_SHOP_OPEN         253
#define IDI_SHOP_CLOSE        220
#define IDI_TRADE_A_UPDATE    18                    // update of thisplayers acception status
#define IDI_LOAD_OPTIONS      152                   // camera angle, sound, mousebutton settings
#define IDI_PRAYER            209
#define IDI_QUESTS            224
#define IDI_BANK_OPEN         93
#define IDI_BANK_CLOSE        171
#define IDI_XP_UPDATE         211
#define IDI_OPEN_DUEL_1       229
#define IDI_CLOSE_DUEL        160
#define IDI_OPEN_TRADE_2      251                   // trade confirmation window
#define IDI_DUEL_UPDATE       63                    // opponents offer was updated
#define IDI_DUELOPT_UPDATE    198                   // update duel options
#define IDI_BANK_UPDATE       139
#define IDI_INV_ADD           228
#define IDI_INV_REMOVE        191
#define IDI_STAT_UPDATE       208
#define IDI_DUEL_B_UPDATE     65                    // update of opponents acception status
#define IDI_DUEL_A_UPDATE     197                   // update of thisplayers acception status
#define IDI_OPEN_DUEL_2       147                   // duel confirmation window
#define IDI_SOUND             11
#define IDI_SPLASH            23
#define IDI_WELCOMEWINDOW     248
#define IDI_MESSAGE_1         148
#define IDI_MESSAGE_2         64
#define IDI_FATIGUE_UPDATE    126
#define IDI_NEW_SLEEPWORD     219
#define IDI_FATIGUE_SLEEPN    168                   // fatigue update in sleeping window
#define IDI_SLEEP_SUCCESS     103
#define IDI_SLEEP_FAILED      15
#define IDI_SYSTEM_UPDATE     172
</pre>
<table border="1" cellpadding="3" cellspacing="3">
<tr>
<td>
<b>opcode</b>
</td>
<td>
<b>usage</b>
</td>
<td>
<b>size</b>
</td>
<td>
<b>payload</b>
</td>
</tr>
<tr>
<td>
</td>
<td>
</td>
<td>
</td>
<td>
</td>
</tr>
</table>

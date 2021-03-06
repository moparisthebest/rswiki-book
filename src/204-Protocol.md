\[\[Category RSC\]\]

This page refers to the RSC \#204 client revision, all of the opcodes
are the same with the exception of the last three in the Outgoing Data
section.

== '''Packet structure''' == ?

== '''Login''' == ?

== '''Incoming Data''' == '''TODO:''' Document packet structures
<pre>
#define IDX_WEIRD_USERNAME    32
#define IDX_LOGIN             0
#define IDO_LOGOUT_ACK        31                    // acknowledge logout command from server
#define IDO_PING              67                    // send ping to server, so it knows we're still there
#define IDO_IGNORE_ADD        132                   // add name to ignore list
#define IDO_IGNORE_REMOVE     241                   // remove name from ignore list
#define IDO_FRIENDS_ADD       195                   // add name to friends list
#define IDO_FRIENDS_REMOVE    167                   // remove name from friends list
#define IDO_PM_FRIEND         218                   // send pm to someone in friends list
#define IDO_SEND_CHAT         216
#define IDO_SEND_SERVER_CMD   38                    // sends a command to the server (type "::xxx" in chat and it sends command 'xxx')
#define IDO_UPDATE_SETTINGS   64                    // changes settings (chatblock, privateblock, tradeblock, duelblock)

#define IDO_LOGOUT            102
#define IDO_CHAR_DESIGN       235                   // send character design (makeover mage, creation)
#define IDO_SLEEPWORD         45
#define IDO_NEW_PLAYER_ACK    163                   // send ids of newly added player back to server, if it wants to

#define IDO_EXCEPTION_SEND    3
#define IDO_WALKCMD_1         16
#define IDO_WALKCMD_2         187
#define IDO_CLICKDIALOGITEM   116
#define IDO_SETCOMBATSTYLE    29
#define IDO_WITHDRAW          22
#define IDO_DEPOSIT           23
#define IDO_CLOSE_BANK        212
#define IDO_BUYITEM           236
#define IDO_SELLITEM          221
#define IDO_CLOSE_SHOP        166
#define IDO_CANCEL_TRADE      230
#define IDO_CONFIRM_TRADE     104
#define IDO_TRADE_UPDATE      46
#define IDO_ACCEPT_TRADE      55
#define IDO_DUEL_CONFIRM_1    77
#define IDO_DUEL_UPDATE       33
#define IDO_DUEL_FLAG_1       8
#define IDO_DUEL_FLAG_2       176
#define IDO_CANCEL_DUEL       197
#define IDO_PRAYER_OFF        254
#define IDO_PRAYER_ON         60
#define IDO_CHANGE_SETTINGS   111

// action commands...
#define IDO_CAST_GR_ITEM      249
#define IDO_USEWITH_GR_ITEM   53
#define IDO_TAKE_ITEM         247
#define IDO_CAST_WALLOBJ      180
#define IDO_USEWITH_WALLOBJ   161
#define IDO_WALLOBJ_CMD1      14
#define IDO_WALLOBJ_CMD2      127
#define IDO_CAST_OBJECT       99
#define IDO_USEWITH_OBJECT    115
#define IDO_OBJECT_CMD1       136
#define IDO_OBJECT_CMD2       79

#define IDO_CAST_INVITEM      4
#define IDO_USEWITH_INVITEM   91
#define IDO_REMOVE_ITEM       170
#define IDO_WEAR_ITEM         169
#define IDO_INVITEM_CMD       90
#define IDO_DROP_ITEM         246

#define IDO_CAST_NPC          50
#define IDO_USEWITH_NPC       135
#define IDO_TALK_NPC          153
#define IDO_NPC_CMD           202
#define IDO_ATTACK_NPC        190

#define IDO_CAST_PLAYER       229
#define IDO_USEWITH_PLAYER    113
#define IDO_ATTACK_PLAYER     171
#define IDO_DUEL_PLAYER       103
#define IDO_TRADE_PLAYER      142
#define IDO_FOLLOW_PLAYER     165

#define IDO_CAST_GROUND       158
#define IDO_CAST_SELF         137

#define IDO_REPORT_ABUSE      206
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

#define IDI_MESSAGE           131                   // (game) messages from server
#define IDI_LOGOUT            4                     // logout command from server (forced, or initiated by client IDO_LOGOUT)
#define IDI_LOGOUT_REJECT     183                   // not allowed to log out (e.g. when in combat)
#define IDI_FRIENDS_LOAD      71                    // when logging in, sends the whole friends list to the client
#define IDI_FRIEND_LOGGED     149                   // a friend from friends list logged in or out (also used to add a friend to friends list)
#define IDI_IGNORE_LOAD       109                   // when logging in, sends the whole ignore list to the client
#define IDI_SETTINGS_LOAD     51                    // load settings upon logging in (blocks)
#define IDI_FRIENDS_PM        120                   // someone pm'd us

#define IDI_PLAYER_MOVEMENT   191                   // player movement update
#define IDI_GRITEMS_UPDATE    99                    // update ground items
#define IDI_OBJECTS_UPDATE    48
#define IDI_INV_LOAD          53                    // load inventory
#define IDI_PLAYER_UPDATE     234
#define IDI_WALLOBJ_UPDATE    91
#define IDI_NPC_MOVEMENT      79                    // npc movement update
#define IDI_NPC_UPDATE        104
#define IDI_DIALOG_SHOW       245
#define IDI_DIALOG_CLOSE      252
#define IDI_LOAD_NEWMAPAREA   25                    // entering a new region (maparea)
#define IDI_XP_LOAD           156                   // load xp and stats
#define IDI_EQUIP_UPDATE      153                   // equipment stats (armour, magic, prayer, weapaim/power)
#define IDI_PLAYER_DIED       83
#define IDI_LOADWORLD         211                   // load objects, wallobjects, items
#define IDI_DESIGN_CHAR       59
#define IDI_OPEN_TRADE_1      92
#define IDI_CLOSE_TRADE       128
#define IDI_TRADE_UPDATE      97                    // opponents offer was updated
#define IDI_TRADE_B_UPDATE    162                   // update of opponents acception status
#define IDI_SHOP_OPEN         101
#define IDI_SHOP_CLOSE        137
#define IDI_TRADE_A_UPDATE    15                    // update of thisplayers acception status
#define IDI_LOAD_OPTIONS      240                   // camera angle, sound, mousebutton settings
#define IDI_PRAYER            206
#define IDI_QUESTS            5
#define IDI_BANK_OPEN         42
#define IDI_BANK_CLOSE        203
#define IDI_XP_UPDATE         33
#define IDI_OPEN_DUEL_1       176
#define IDI_CLOSE_DUEL        225
#define IDI_OPEN_TRADE_2      20                    // trade confirmation window
#define IDI_DUEL_UPDATE       6                     // opponents offer was updated
#define IDI_DUELOPT_UPDATE    30                    // update duel options
#define IDI_BANK_UPDATE       249
#define IDI_INV_ADD           90
#define IDI_INV_REMOVE        123
#define IDI_STAT_UPDATE       159
#define IDI_DUEL_B_UPDATE     253                   // update of opponents acception status
#define IDI_DUEL_A_UPDATE     210                   // update of thisplayers acception status
#define IDI_OPEN_DUEL_2       172                   // duel confirmation window
#define IDI_SOUND             204
#define IDI_SPLASH            36
#define IDI_WELCOMEWINDOW     182
#define IDI_MESSAGE_1         89
#define IDI_MESSAGE_2         222
#define IDI_FATIGUE_UPDATE    114
#define IDI_NEW_SLEEPWORD     117
#define IDI_FATIGUE_SLEEPN    244                   // fatigue update in sleeping window
#define IDI_SLEEP_SUCCESS     84
#define IDI_SLEEP_FAILED      194
#define IDI_SYSTEM_UPDATE     52

#define IDX_ACCOUNT_STOLEN    18                // "Account suspected stolen.", "Press 'recover a locked account' on front page."
#define IDX_ACCOUNT_NOT_RSC   21                // "Unable to login.", "That is not an RS-Classic account"
#define IDX_PASSWD_STOLEN     22                // "Password suspected stolen.", "Press 'change your password' on front page."
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

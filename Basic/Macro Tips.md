## Creating a Macro

Type / macro or click on the talk button and select Macro. A window will appear listing the macros. In the beginning, you will not have macros.
Click the "new" button at the bottom of this window. Another window will appear in which you can enter a name for the new Macro and select an icon.
Enter the name of the Macro. Choose it in a way that makes it clear what it does. For example, enter the name "assist" (help).
Select an icon. For example, a sword.
Click "Okay" - now you will see the Macros window with the selected icon (sword) and the entered name ("assist").
Left-click (LMB) on the macro icon to select it. A button will appear, with which you can change the name of the macro or its icon.
While the icon for your macro is highlighted, move the cursor to the "enter macro commands" input area (enter macro commands). This is where you can enter what Macro should do when you click on its icon. You need to add a "/" before the command, if it requires it. In general, commands must be entered in the same way as in their normal use.
Enter "/ assist Nebu"
Now, place the cursor over the sword icon (assist), then click on it with the LMB and hold it (LMB).
Move the icon to an empty space in the action bar.

To use your new macro, click the corresponding number button or right-click (RMB) on the macro icon in the shortcut bar.
Now, you have a Macro with which you can help another player (Nebu) in attacking monsters. When Nebu enters a battle with someone, press the button of this Macro and your new target will be the subject that Nebu is fighting.

## Finishing Editing Macros
After you finish editing or creating Macros, click the cross in the upper right corner of the Macros window to close it.

## Editing Existing Macros
Type / macro and then click on the macro icon you want to edit. You can now edit the selected Macro in the "Enter Macro Commands" input area. When you are done, click the cross located in the upper right corner of the Macros window to close it.

## Limitations of Macros
For each Macro there is a limit on the number of characters. If your Macro is too long, make it shorter (approx. Transl. - mdya ... and we will not guess before)!

## Macro Tips
Use any existing commands.

## Here are some other tips for using macros:

- repeating text that you do not want to enter again
repetition messages for auctions
-creation of funny messages
-execution of a sequence of commands, for example:
```
/leave 1 
/leave 2 (leave channels 1 and 2)
/join wowtraders (joins the wowtraders channel)
/g Hello everyone! (welcome everyone to your guild channel)
```

## Additional Information

You can use "% t" in your Macros to automatically insert the selected monster, creature, player into your Macro. For example, the macro "/ say hi% t" will display "Hi Nebu" if you have currently selected the Nebu player.

/ cast allows you to cast spells by name. Type "/ cast (spell name)" - Example "/ cast Fireball (Rank 1)". To use this command in macros, you can type it in "pens", or click on a spell holding Shift in the spell book to automatically add the corresponding command to the macro.


## Basics:
Macros in the Islands are written in the Lua language (www.lua.org). Lua is a small and fast, but powerful enough language written in C. Therefore, knowing at least the basics of C? You can easily understand this simple task - writing macros for Islands.
Type in the chat / macros line - a list of macros will open, type the new button, then create a name, select a picture, then enter the code. Stop, and what actually enter? Well, let us think at all, why do we need all this, correctly, to automate our actions, and what they can be read in this topic. The first thing that comes to mind is to tell your group 
## who to attack:
```
/p Atacking% t
```
(% t substitutes the name of the character you selected.)
Well, now let's say we are a magician, who played a magician - he knows what a misfortune to cast polymorph in a group, when members of the group, by inconsistency, begin to attack and quite often they get a sheep.

```
/p Polymorphing! DONT atack% t!
/cast Polymorph (Rank X)
```
(X is your spell level)
Go ahead. We need a script that treated and warned the rest of the healers that you are already curing this goal:

```
/ script if ((UnitName ("target") ~ = nil) AND (UnitIsFriend ("player", "target"))
then SendChatMessage ("Healing (+ n)!", "PARTY", "COMMON", UnitName ("target")); end
/ cast SpellName (Rank X)
```
I think it is clear, the description of the function, see below.


## Another useful macro:
```
/ script ToggleBag (0);
/ script ToggleBag (1);
/ script ToggleBag (2);
/ script ToggleBag (3);
/ script ToggleBag (4);
```
Opens / closes all bags. It is useful to bind to "b".


## I will give the main functions:
Although these are all functions, some of them are only informational, and some directly affect the game, so I divided everything into methods and properties for convenience.


## [actions]
AttackTarget ();
Example: AttackTarget ();
Description: Attacks the selected character.

CastSpellByName (spellname)
Example: CastSpellByName ("Demon Skin");
Description: Casts the spell indicated.

TargetUnit (targetcode);
Example: TargetUnit ("player");
Description: Select the character specified in the parameter "player", "party1" .. "party5", "npc", "target".

TargetUnitsPet (targetcode);
Example: TargetUnitsPet ("player");
Description: Selects a character's pet.

TargetLastEnemy ();
Example: TargetLastEnemy ();
Description: Highlights the last character attacked.

AssistUnit (target)
Example: AssistUnit ("target");
Description: Helps to attack the character specified in the parameter.

AssistByName (target)
Example: AssistByName ("Marco");
Description: Helps to attack the character with the name specified in the parameter.

FollowUnit (target)
Example: FollowUnit ("target");
Description: It follows the character specified in the parameter.

FollowUnitByName (target)
Example: FollowByName ("Beeblebrox");
Description: It follows the character with the name specified in the parameter.

ToggleBag (bagnumber)
Example: ToggleBag (0);
Description: Opens / closes bag bags located: 4-3-2-1-0. 0 is a backpack.


## [group and interaction]
InviteByName (target)
Example: InviteByName (GetSlashCmdTarget (msg));
Description: Invites a character to a group with the name specified in the parameter.

UninviteByName (target)
Example: UninviteByName (GetSlashCmdTarget (msg));
Description: Removes from the group the character with the name specified in the parameter.

InitiateTrade (target)
Example: InitiateTrade ("target");
Description: Invites to trade the character specified in the parameter.

InspectUnit (target)
Example: InspectUnit ("target");
Description: Displays information about the character.

BeginTrade ();
Description: Agree to trade.

CancelTrade ();
Description: Refuse to trade.

AcceptGroup ()
Description: Agree to an invitation to the group.

DeclineGroup ()
Description: Abandon the group

PromoteToPartyLeader (unit);
Description: Makes the specified player a leader.

LeaveParty ()
Description: Leave the group.

AddFriend (name)
Description: Add a friend.

RemoveFriend (name)
Description: Delete Friend

AddOrDelIgnore (name);
Description: Adds / removes a player from the ignore list.

Duel (name)
Description: Causes a player to a duel.

CancelDuel ();
Description: Cancels the duel.

SetLootMethod (methodstring, player)
Description: Sets the loot method: "freeforall", "roundrobin", "master".

LootSlot (slotidnumber, 0)
Example: LootSlot (((LOOTFRAME_NUMBUTTONS - 1) * (LootFrame.page - 1)) + this: GetID (), 0);
Description: Lost item


## [Movement]
MoveForwardStart (starttime);
Description: The player begins to run forward.

MoveForwardStop (time);
Description: The player stops running forward.

MoveBackwardStart (starttime);
Description: The player begins to run backwards.

MoveBackwardStop (stoptime);
MoveBackwardStop (arg1);
Description: The player stops running back.

TurnLeftStart (starttime);
Description: The player begins to run to the left.

TurnLeftStop (arg1);
Description: The player stops running to the left.

TurnRightStart (starttime);
Description: The player begins to run to the right.

TurnRightStop (stoptime);
Description: The player stops running to the right.

StrafeLeftStart (StartTime);
Description: The player starts to look left.

StrafeLeftStop (stoptime);
Description: The player stops playing left.

StrafeRightStart (starttime);
Description: The player begins to straifit right.

StrafeRightStop (stoptime);
Description: The player stops right-clicking.

Jump ();
Description: Makes a player jump.

SitOrStand ()
Description: Makes sit down / stand up


## [guild]
AcceptGuild ()
Description: Accepts an invitation to the guild.

DeclineGuild ()
Description: Refuses an invitation to the guild.

GuildInviteByName (player);
Description: Invitation to the guild for the player whose name is specified in the parameter.

GuildUninviteByName (player)
Description: Expels a player from the guild whose name is specified in the parameter.

GuildPromoteByName (player)
Description: Increases the status of the player whose name is specified in the parameter.

GuildDemoteByName (player)
Description: Reduces the status of the player whose name is specified in the parameter.

GuildSetLeaderByName (player)
Description: Makes the leader the player whose name is specified in the parameter.

GuildSetMOTD (message)
Description: Sets the welcome message.

GuildLeave ()
Description: Leave the guild.

## [Pet]
PetAttack ();
Description: Makes your pet attack.
PetAbandon ();
Description: Throw your pet.

PetRename (name)
Description: Rename your pet.

PetPassiveMode ();
Description: Switches your pet to passive mode.

PetDefensiveMode ()
Description: Switches your pet to protection mode.

PetAggressiveMode ()
Description: Switches your pet to aggressive mode.

PetWait ()
Description: Stops your pet in passive mode.

PetFollow ()
Description: Makes your pet follow you.


## [different]
SendChatMessage (msg, mode, language, channel);
Example: SendChatMessage (msg, "WHISPER", this.language, lastTell);
Description: Sends message mode: "SAY", "YELL", "PARTY", "AFK", "DND", language: "COMMON", "DRACONIC", "ORCISH" ...

RandomRoll (low, high);
Example: RandomRoll ("1", "100");
Description: It gives a random number, convenient when drawing chests.

PlaySound (filename);
Example: PlaySound ("BAGMENUBUTTONPRES");
Description: Plays a sound file.

Screenshot ();
Description: Makes a screenshot.

ForceLogout ()
Description: Enhanced disconnect.

Logout ()
Description: Disconnect.

Quit ()
Description: Exit the game


## [Properties]
UnitName (string)
Example: target = UnitName ("target");
Description: Returns Player Name

GetFriendInfo (friendid)
Example: name, level, class, area, connected = GetFriendInfo (friendIndex);
Description: Returns information about a friend.

UnitXP (target)
Example: local currXP = UnitXP ("player");
Description: Returns Player Experience

UnitXPMax (target)
Example: local nextXP = UnitXPMax ("player");
Description: Shows the maximum player experience.

GetUnitMoney (target)
Example: if (UnitMoney ("player")> = moneyCost) then
Description: Shows the amount of player money.

UnitExists (unitname)
Example: if (UnitExists (unit) and UnitIsPlayer (unit)) then
Description: Returns true if the character exists.

UnitIsPlayer (unitname)
Example: if (UnitExists (unit) and UnitIsPlayer (unit)) then
Description: Returns true if the character is a player.

PetCanBeAbandoned ()
Description: Returns true if the pet can be thrown.

UnitIsUnit (unitnamea, unitnameB)
Example: UnitIsUnit ("target", "pet")
Description: Returns true if unitnamea is unitnameB

UnitReaction ("target", "player")
Example: UnitReaction ("target", "player")
Description: Returns the behavior type: neutral hostile, friendly.

GuildInfo ()
Description: Shows guild info

GetPartyMember (index [or id])
Example: GetPartyMember (3)
Description: Returns the name of the party member.

[B] UnitIsPartyLeader (unitname)
Example: UnitIsPartyLeader ("target")
Description: Returns true if the character is the leader of the group.

GetLootMethod ()
Example: lootMethod, lootMaster = GetLootMethod ();
Description: Returns the type and master (if any) of the loot

UnitInParty (unitname)
Example: UnitInParty ("target")
Description: Returns true if the character is in a group.

GetPlayerMapPosition (playerid);
Example: playerX, playerY = GetPlayerMapPosition ("player");
Description: Returns your coordinates.

GetCorpseMapPosition ();
Example: corpseX, corpseY = GetCorpseMapPosition ();
Description: Returns the coordinates of your body.


## [chanel]
LeaveChannelByName (channelname)
LeaveChannelByName ("Trade");
Leaves the channel with the specified name.

ListChannelByName (channelname)
ListChannelByName ("trad")
Lists all match the specified regular expression.

ListChannels ()
ListChannels ();
Lists all of the channel.

SetChannelPassword (username, password)
SetChannelPassword ("Xiphoris", "cantkeepassecret") l
This is a legal action.

ChannelModerator (channel, player)
ChannelModerator ("uimods", "Kelthan");
Sets the specified player as the channel moderator.

ChannelUnmoderator (channel, player)
ChannelUnmoderator ("uimods", "xiphoric");
Takes the specified user away from the moderator status.


ChannelMute (channel, player)
ChannelMute ("uimods", "zileas");
Turns off the player's ability to speak in a channel.

ChannelUnmute (channel, player)
ChannelUnmute ("uimods", "marco");
Unmutes the specified user from the channel.

ChannelInvite (channel, player)
ChannelInvite ("cutestelves", "glorfindel");
Invites the user to the chatroom.

ChannelKick (channel, player)
ChannelKick ("bigllamas", "Strong_Bad_Is_Geh");
Kicks the specified user from the channel.

ChannelBan (channel, player)
ChannelBan ("uimods", "alexyoshi")
Bans a player from the specified channel.

ChannelUnban (channel, player)
ChannelUnban ("uimods", "kat");
Unbans a player from a channel.

ChannelToggleAnnouncements (channel);
ChannelToggleAnnouncements (channel);
Sets the channel to display announcements.
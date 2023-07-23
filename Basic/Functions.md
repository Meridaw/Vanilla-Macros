## Action Functions
These functions are those which operate with the action buttons
```
UI ActionButtonDown(id)   - Press the specified action button.
UI ActionButtonUp(id)   - Release the specified action button.
ActionHasRange(slot)   - Determine if the specified action is a range restriction (1 if yes, nil if no)
UI BonusActionButtonDown - Trigger the specified bonus(pet or minion) action button.
UI BonusActionButtonUp - Release the specified bonus(pet or minion) action button.
PROTECTED CameraOrSelectOrMoveStart()   - Begin "Left click" in the 3D world. (1.10 - Protected)
PROTECTED CameraOrSelectOrMoveStop([stickyFlag])   - End "Left click" in the 3D world. (1.10 - Protected)
ChangeActionBarPage()   - Changes the current action button set to CURRENT_ACTIONBAR_PAGE.
GetActionBarToggles()   - Return the toggles for each action bar.
GetActionCooldown(slot)   - This returns the cooldown values of the specified action..
GetActionCount(slot)   - Get the count (bandage/potion/etc) for an action, returns 0 if none or not applicable.
GetActionText(slot)   - Get the text label (macros, etc) for an action, returns nil if none.
GetActionTexture(slot)   - Gets the texture path for the specified action.
GetBonusBarOffset()   - Determine which page of bonus actions to show.
HasAction(slot)   - Returns 1 if the player has an action in the specified slot, nil otherwise.
IsActionInRange(slot)   - Test if an action is in range (1=yes, 0=no, nil=not applicable).
IsAttackAction(slot)   - Return 1 if an action is an 'attack' action (flashes during combat), nil otherwise.
IsAutoRepeatAction(slot)   - Return 1 if an action is auto-repeating, nil otherwise.
IsCurrentAction(slot)   - Return 1 if an action is the one currently underway, nil otherwise.
IsUsableAction(slot)   - Return 1 if an action can be used at present, nil otherwise.
IsConsumableAction(slot)   - Return 1 if an action is consumable (i.e. has a count), nil otherwise.
IsEquippedAction(slot)   - Return 1 if an action is equipped (i.e. connected to an item that must be equipped), nil otherwise.
PetHasActionBar()   - Determine if player has a pet with an action bar.
PickupAction(slot)   - Drags an action out of the specified quickbar slot and holds it on the cursor.
PickupPetAction(slot)   - Drags an action from the specified pet action bar slot into the cursor.
PlaceAction(slot)   - Drops an action from the cursor into the specified quickbar slot.
SetActionBarToggles(show1,show2,show3,show4[, alwaysShow])   - Set show toggle for each action bar   - 'alwaysShow' added in 1.12
PROTECTED TurnOrActionStart()   - Begin "Right Click" in the 3D world. (1.10 - Protected)
PROTECTED TurnOrActionStop()   - End "Right Click" in the 3D world. (1.10 - Protected)
UseAction(slot[, checkCursor[, onSelf]])   - This instructs the interface to use the action associated with the specified ID, optionally on the player (regardless of target).
```

## Activity Functions
This section is for functions which make the player do something
```
AcceptDuel()   - The player accepts the challenge to duel.
AttackTarget()   - Attacks the targetted unit.
CancelDuel()   - Refuse the invitation to fight a duel.
CancelLogout()
CancelMeetingStoneRequest()   - Remove character from an instance's Meeting Stone queue
ClearTutorials()
ConfirmSummon()
FlagTutorial("tutotial")
PROTECTED ForceLogout()
ForceQuit()
GetSummonConfirmAreaName()
GetSummonConfirmSummoner()
GetSummonConfirmTimeLeft()
Logout - Logs the user out of the game.
Quit - Quits the application, NOT the LUA script.
RandomRoll(low, high)   - Does a random roll between the two values.
SitOrStand()   - The player sits or stands.
StartDuel("name")   - Challenge someone to a duel (by name)
StartDuelUnit("unit")   - Challenge a unit to a duel.
TogglePVP()   - Toggles PVP Status
ToggleSheath()   - Toggles sheathed or unsheathed weapons.
UseSoulstone()   - Use an active soulstone to resurrect yourself after death.
```

## AddOn Functions
```
DisableAddOn(index or "AddOnName")   - Disable the specified AddOn for subsequent sessions.
DisableAllAddOns()   - Disable all AddOns for subsequent sessions.
EnableAddOn(index or "AddOnName")   - Enable the specified AddOn for subsequent sessions.
EnableAllAddOns()   - Enable all AddOns for subsequent sessions.
GetAddOnDependencies(index or "AddOnName")   - Get dependency list for an AddOn.
GetAddOnInfo(index or "AddOnName")   - Get information about an AddOn.
GetAddOnMetadata(index or "name", "variable")   - Retrieve metadata from addon's TOC file.
GetNumAddOns()   - Get the number of user supplied AddOns.
IsAddOnLoaded(index or "AddOnName")   - Returns true if the specified AddOn is loaded.
IsAddOnLoadOnDemand(index or "AddOnName")   - Test whether an AddOn is load-on-demand.
LoadAddOn(index or "AddOnName")   - Request loading of a Load-On-Demand AddOn.
ResetDisabledAddOns() -
```

## Auction Functions
```
CalculateAuctionDeposit(runTime)   - Returns the required deposit for the current selling item given the specified duration (minutes).
CanSendAuctionQuery()   - Return 1 if auction search button would be active, nil otherwise.
CancelAuction(index)   - Cancel the specified auction (on the "owner" list).
ClickAuctionSellItemButton()   - Puts the currently 'picked up' item into the 'create auction' slot.
CloseAuctionHouse()   - Will close the AuctionFrame if opened.
GetAuctionHouseDepositRate()   - Returns the deposit rate (percentage) for the currently open auction house (Possibly out-dated by CalculateAuctionDeposit).
GetAuctionInvTypes(classIndex, subclassIndex)   - Returns types of subcategories items.
GetAuctionItemClasses()   - Returns major auction item categories.
GetAuctionItemInfo("type", index)   - Returns details about the specified auction item.
GetAuctionItemLink("type", index)   - Returns an itemLink for the specified auction item.
GetAuctionItemSubClasses(classIndex)   - Returns subcategories in the nth auction category.
GetAuctionItemTimeLeft("type", index)   - Returns the time left status of the specified auction item.
GetAuctionSellItemInfo()   - Returns information about the current selling item (or nil if none selected).
GetBidderAuctionItems([page])   - ?.
GetNumAuctionItems("type")   - Returns the size of the specified auction item list.
GetOwnerAuctionItems([page])   - ?.
GetSelectedAuctionItem("type")   - Returns the index (1-50) of the selected auction item or 0 if none is selected.
IsAuctionSortReversed("type", "sort")   - Returns 1 if the specified auction list and sort is reversed, nil otherwise.
PlaceAuctionBid("type", index, bid)   - Place a bid on the selected auction item.
QueryAuctionItems("name", minLevel, maxLevel, invTypeIndex, classIndex, subclassIndex, page, isUsable, qualityIndex)   - ?.
SetSelectedAuctionItem("type", index)   - ?.
SortAuctionItems("type", "sort")   - Request that the specified auction list be sorted by a specific column.
StartAuction(minBid, buyoutPrice, runTime)   - Starts the auction you have created in the Create Auction panel.
UI AuctionFrameAuctions.duration - Set the amount of time the auction will run for in minutes.
```

## Bank Functions
```
BankButtonIDToInvSlotID(buttonID)   - Returns the ID number of a bank button in terms of inventory slot ID.
CloseBankFrame()   - Close the bank frame if it's open. --Ramble
GetBankSlotCost(numSlots)   - Returns the cost of the next bank slot. --Ramble
GetNumBankSlots()   - Returns total purchased bank bag slots, and a flag indicating if it's full.
PurchaseSlot()   - Buys another bank slot if available..
```

## Battlefield Functions
```
AcceptAreaSpiritHeal()   - Accept a spirit heal.
CancelAreaSpiritHeal()   - Cancel a spirit heal.
CanJoinBattlefieldAsGroup()   - returns nil if the player can not do a group join for a battlefield.
AcceptBattlefieldPort(index[, acceptFlag])   - Accept or reject an offered battlefield port.
CheckSpiritHealerDist()   - Return true if you are in range with spirit healer while dead.
CloseBattlefield()   - ?.
GetAreaSpiritHealerTime()   - Returns the time left until the next resurrection by the Sprit Guide.
GetBattlefieldEstimatedWaitTime(index)   - Get the estimated wait for entry into the battlefield.
GetBattlefieldFlagPosition(index)   - Get the map position of the flag.
GetBattlefieldInfo(index)   - Returns detailed information on the Battlefield you last opened a queue window for.
GetBattlefieldInstanceExpiration()   - Get shutdown timer for the battlefield instance.
GetBattlefieldInstanceInfo(index)   - Get the instance ID for a battlefield.
GetBattlefieldInstanceRunTime()   - In milliseconds, the time since battleground started. (seems to be queried from server because it is not in sync with time())
GetBattlefieldPortExpiration(index)   - Get the remaining milliseconds before the battlefield port expires.
GetBattlefieldPosition(index)   - Get the map position and name of a player in the battleground not in your raid.
GetBattlefieldScore(index)   - Get score information about a player.
GetBattlefieldStatData(playerIndex, slotIndex)   - Get information for a player from a colum thats specific to a battleground. (like Warsong Gulch flag captures)
GetBattlefieldStatInfo(index)   - Get the battleground specific column for the score board.
GetBattlefieldStatus(index)   - Get the battlefield's current status.
GetBattlefieldTimeWaited(index)   - Get time waited in queue in milliseconds.
GetBattlefieldWinner()   - Get the battlefields winner.
GetNumBattlefieldFlagPositions()   - Get the number of flag positions available from GetBattlefieldFlagPosition().
GetNumBattlefieldPositions()   - Get the number of positions available from GetBattlefieldPosition().
GetNumBattlefieldScores()   - Returns the number of scores(players) listed in the battlefield scoreboard.
GetNumBattlefieldStats()   - Get the number of battleground specific columns.
GetNumBattlefields()   - Get the number of running battlefields for the last battleground queue window you opened.
GetSelectedBattlefield()   - Get the selected battlefield to join first.
GetWorldStateUIInfo(i)   - Get score and flag status within a battlefield.
JoinBattlefield(index[, joinAs])   - Queue for a battleground either solo or as a group.
LeaveBattlefield()   - Leave the current battlefield if it's been won.
RequestBattlefieldPositions()   - Request new data for GetBattlefieldPosition().
RequestBattlefieldScoreData()   - Request new data for GetBattlefieldScore().
SetBattlefieldScoreFaction([faction])   - Set the faction to show on the battlefield scoreboard.
SetSelectedBattlefield(index)   - Select the battlefield instance you want to join or the first one that becomes available.
ShowBattlefieldList(index)   - Displays a queue window for the specified battlefield. Only works if you are already in a queue for the battlefield. Index corresponds to location in queue array.
ToggleBattlefieldMinimap()   - Toggles the Battlefield Minimap.
```

## Buff/Debuff Functions
```
CancelPlayerBuff(buffIndex)   - Removes a specific buff from the player.
CancelTrackingBuff()   - Cancels your current tracking buff (Find Minerals etc.)
GetPlayerBuff(buffId, buffFilter)   - Retrieves info about a certain effect (beneficial, harmful or passive)
GetPlayerBuffApplications(buffIndex)   - Retrieves the number of applications of a debuff or buff.
GetPlayerBuffDispelType(buffIndex)   - Get the debuff type for a player debuff ("Magic", "Curse", "Disease", or "Poison")
GetPlayerBuffTexture(buffIndex)   - Retrieves the texture identifier for a certain buff
GetPlayerBuffTimeLeft(buffIndex)   - Retrieves how long a buff will last before expiring
GetWeaponEnchantInfo()   - Return information about main and offhand weapon enchantments.
UnitBuff("unit", index[, showCastable])   - Retrieves info about a buff of a certain unit.
UnitDebuff("unit", index[, showDispellable])   - Retrieves info about a debuff of a certain unit.
```

## Camera Functions
```
PROTECTED CameraOrSelectOrMoveStart()   - Begin "Left click" in the 3D world. (1.10 - Protected)
PROTECTED CameraOrSelectOrMoveStop([stickyFlag])   - End "Left click" in the 3D world. (1.10 - Protected)
CameraZoomIn(increment)   - Zooms the camera into the viewplane by increment.
CameraZoomOut(increment)   - Zooms the camera out of the viewplane by increment.
FlipCameraYaw(degrees)   - Rotates the camera about the Z-axis by the angle amount specified in degrees.
IsMouselooking()   - Returns 1 if mouselook is currently active, nil otherwise.
MouselookStart()
MouselookStop()
MoveViewDownStart()   - Begins rotating the camera downward.
MoveViewDownStop()   - Stops rotating the camera after MoveViewDownStart() is called.
MoveViewInStart()   - Begins zooming the camera in.
MoveViewInStop()   - Stops zooming the camera in after MoveViewInStart() is called.
MoveViewLeftStart()   - Begins rotating the camera to the Left.
MoveViewLeftStop()   - Stops rotating the camera after MoveViewLeftStart() is called.
MoveViewOutStart()   - Begins zooming the camera out.
MoveViewOutStop()   - Stops zooming the camera out after MoveViewOutStart() is called.
MoveViewRightStart()   - Begins rotating the camera to the Right.
MoveViewRightStop()   - Stops rotating the camera after MoveViewRightStart() is called.
MoveViewUpStart()   - Begins rotating the camera upward.
MoveViewUpStop()   - Stops rotating the camera after MoveViewUpStart() is called.
PROTECTED PitchDownStart()   - Begins pitching the camera Downward.
PROTECTED PitchDownStop()   - Stops pitching the camera after PitchDownStart() is called.
PROTECTED PitchUpStart()   - Begins pitching the camera Upward.
PROTECTED PitchUpStop()   - Stops pitching the camera after PitchUpStart() is called.
NextView()   - Cycles forward through the five predefined camera positions.
PrevView()   - Cycles backward through the five predefined camera positions.
ResetView(index)   - Resets the specified (1-5) predefined camera position to it's default if it was changed using SaveView(index).
SaveView(index)   - Replaces the specified (1-5) predefined camera positions with the current camera position.
SetView(index)   - Sets camera position to a specified (1-5) predefined camera position.
```

## Channel Functions
These are chat functions which are specific to channels.
```
AddChatWindowChannel(chatFrameIndex, "channel")   - Make a chat channel visible in a specific ChatFrame.
ChannelBan("channel", "name")   - Bans a player from the specified channel.
ChannelInvite("channel", "name")   - Invites the specified user to the channel.
ChannelKick("channel", "name")   - Kicks the specified user from the channel.
ChannelModerate("channel")   - Enables channel Moderation commands such as ChannelKick/Ban.
ChannelModerator("channel", "name")   - Sets the specified player as the channel moderator.
ChannelMute("channel", "name")   - Turns off the specified player's ability to speak in a channel.
ChannelToggleAnnouncements("channel")   - Toggles the channel to display announcements either on or off.
ChannelUnban("channel", "name")   - Unbans a player from a channel.
ChannelUnmoderator("channel", "name")   - Takes the specified user away from the moderator status.
ChannelUnmute("channel", "name")   - Unmutes the specified user from the channel.
DisplayChannelOwner("channel")   - Displays the owner of the specified channel in the default chat.
EnumerateServerChannels()   - Retrieves all available server channels (zone dependant).
GetChannelList()   - Retrieves joined channels.
GetChannelName("channel" or index)   - Retrieves the name from a specific channel.
GetChatWindowChannels(index)   - Get the chat channels received by a chat window.
JoinChannelByName("channel"[, "password"[, frameId]])   - Join the specified chat channel (with optional password, and register for specified frame) (updated in 1.9)
LeaveChannelByName("channel")   - Leaves the channel with the specified name.
ListChannelByName(channelMatch)   - Lists members in the given channel to the chat window. -- Mjt 12:39, 19 June 2006 (EDT)
ListChannels()   - Lists all of the channels into the chat window.
RemoveChatWindowChannel(chatFrameIndex, "channel")   - Make a chat channel invisible (hidden) in a specific ChatFrame.
SendChatMessage("text"[, "type"[, language[, targetPlayer, ...]]])   - Sends a chat message.
SetChannelOwner("channel", "name")   - Sets the channel owner.
SetChannelPassword("channel", "password")   - Changes the password of the current channel.
```

## Character Functions
```
AbandonSkill(index)   - The player abandons a skill.
AcceptResurrect()   - The player accepts the request from another player to resurrect him/herself.
AcceptSkillUps()
AcceptXPLoss()   - Accept the XP loss to be reborn by a spirit healer (The name is somewhat of a misnomer, since it's now durability rather than XP that is lost).
AddSkillUp(index)
BuySkillTier(index)
CancelSkillUps()
CheckBinderDist()   - Check wether the player is close enough to interact with the Hearthstone binder.
ConfirmBinder()   - Confirm the request to set the binding of the player's Hearthstone.
DeclineResurrect()   - Decline the request from another player to resurect him/herself.
GetBindLocation()   - Get the name of the location for your Hearthstone.
GetBlockChance()   - Returns the player's percentage block chance.
GetComboPoints()   - Get the current number of combo points.
GetCorpseRecoveryDelay()   - Time left before a player can accept a resurrection
GetDamageBonusStat()   - returns index of which stat a player receives a damage bonus from increasing
GetDodgeChance()   - Returns the player's percentage dodge chance.
GetMoney()   - Returns an integer value of your held money in copper.
GetParryChance()   - Returns the player's percentage parry chance.
GetReleaseTimeRemaining()   - Returns the amount of time left before your ghost is pulled from your body.
GetResSicknessDuration()
GetRestState()
GetTimeToWellRested()
GetXPExhaustion()   - Returns your character's current rested XP, nil if character is not rested.
HasFullControl()
HasSoulstone()
IsResting()
NotWhileDeadError()   - Generates an error message saying you cannot do that while dead.
RemoveSkillUp(index)
ResurrectHasSickness()   - Appears to be used when accepting a resurrection will give you resurrection sickessness.
ResurrectHasTimer()   - Does the player have to wait before accepting a resurrection
RetrieveCorpse()   - Resurrects when near corpse. e.g., The "Accept" button one sees after running back to your body.
SetSelectedSkill(index)
```

## Chat Window Functions
These are functions which are specific to chat window management.
```
AddChatWindowChannel(chatFrameIndex, "channel")   - Make a chat channel visible in a specific ChatFrame.
AddChatWindowMessages - Adds a messaging group to the specified chat window.
ChangeChatColor(chatType,r,g,b)   - Update the color for a type of chat message.
UI ChatFrame_AddChannel(chatFrame, "channelName")   - Activate channel in chatFrame.
UI ChatFrame_OnHyperlinkShow(reference, link, button)   - called when the user clicks on a chatlink.
GetChatTypeIndex(type)   - Get the numeric ID of a type of chat message.
GetChatWindowChannels(index)   - Get the chat channels received by a chat window.
GetChatWindowInfo(index)   - Get setup information about a chat window.
GetChatWindowMessages(index)   - Get the chat message types received by a chat window.
JoinChannelByName("channel"[, "password"[, frameId]])   - Join the specified chat channel (with optional password, and register for specified frame) (updated in 1.9)
LoggingChat(newState)   - Gets or sets whether logging chat to Logs\WoWChatLog.txt is enabled.
LoggingCombat(newState)   - Gets or sets whether logging combat to Logs\WoWCombatLog.txt is enabled.
RemoveChatWindowChannel(chatFrameIndex, "channel")   - Make a chat channel invisible (hidden) in a specific ChatFrame.
RemoveChatWindowMessages(chatFrameIndex,"messageGroup")   - Remove a set of chat messages from this window.
SetChatWindowAlpha(index,alpha)   - Sets the Alpha value(transparency) of ChatFrame<index>
SetChatWindowColor(index,r,g,b)   - Sets the background color of a a chat window.
SetChatWindowDocked(index,docked)   - Set whether a chat window is docked.
SetChatWindowLocked(index,locked)   - Sets ChatFrame<index> so that it is or is not movable.
SetChatWindowName(index,"name")   - Sets the name of ChatFrame<index> to <"name">.
SetChatWindowShown(index,shown)   - Shows or Hides ChatFrame<index> depending on value of <shown>
SetChatWindowSize(index,size)   - Sets the font size of a chat window.
```

## Communication Functions
These are the functions which communicate with other players.
```
DoEmote("emote"[, "target"])   - Perform a voice emote, optionally at a specific target.
GetDefaultLanguage("unit")   - Returns the default language that the unit is speaking after logon.
GetLanguageByIndex(index)   - Returns the language specified by the index.
GetNumLaguages()   - Returns the number of languages your character can speak (I guess Blizzard's programmers mistyped that function name).
RandomRoll(low, high)   - Does a random roll between the two values.
SendAddonMessage("prefix", "text", "type")   - Sends a message to hidden AddOn channels.   - Added in 1.12
SendChatMessage("text"[, "type"[, language[, targetPlayer]]])   - Sends a chat message.
```

## Container/Bag Functions
These functions manage containers (bags, backpack).
```
ContainerIDToInventoryID(bagID)
GetBagName(bagID)   - Get the name of one of the player's bags.
GetContainerItemCooldown(bagID, slot)
GetContainerItemInfo(bagID, slot)   - Get the info for an item in one of the player's bags.
GetContainerItemLink(bagID, slot)   - Returns the itemLink of the item located in bag#, slot#.
GetContainerNumSlots(bagID)   - Gives you the number of slots available in the bag specified by the index.
HasKey()   - Returns 1 if the player has a keyring, nil otherwise.
UI OpenAllBags()   - Open/Close all bags
PickupBagFromSlot(slot)   - Picks up the bag from the specified slot, placing it in the cursor. If an item is already picked up, this places the item into the specified slot, swapping the items if needed.
PickupContainerItem(bagID,slot)
PutItemInBackpack()   - attempts to place item in backpack (bag slot 0).
PutItemInBag(inventoryId)   - attempts to place item in a specific bag.
SetBagPortaitTexture(texture,slot)
SplitContainerItem(bagID,slot,amount)
UI ToggleBackpack()   - Toggles your backpack open/closed.
UI ToggleBag(bagID)   - Opens or closes the specified bag.
UseContainerItem(bagID, slot[, onSelf])   - Uses an item located in bag# and slot#. (Warning: If a vendor window is open, using items in your pack may sell them!)   - 'onSelf' added in 1.12
```

## Crafting Functions
These superseded the older crafting functions for all skills, except for enchanting and the hunters train-pet-window. Most functions only work if the window for enchants is opened in the GUI. You can check whether the window is opened by using GetCraftSkillLine().
```
CloseCraft()
CollapseCraftSkillLine(index)
DoCraft(index)
ExpandCraftSkillLine(index)
GetCraftButtonToken()
GetCraftDescription(index)
GetCraftDisplaySkillLine()
GetCraftIcon(index)
GetCraftInfo(index)
GetCraftItemLink(index)   - Returns an itemLink for the specified craftable item.
GetCraftName()
GetCraftNumReagents(index)
GetCraftReagentInfo(index,reagentIndex)
GetCraftReagentItemLink(index,reagentIndex)   - Returns an itemLink for one of the reagents needed to craft the given item
GetCraftSelectionIndex()
GetCraftSkillLine()
GetCraftSpellFocus(index)   - ?.
GetNumCrafts()
SelectCraft(index)
```

## Cursor Functions
```
AutoEquipCursorItem()   - Causes the equipment on the cursor to be equipped.
ClearCursor()   - Clears whatever item the cursor is dragging from the cursor.   - Added in 1.12
CursorCanGoInSlot(invSlot)   - Return true if the item currently held by the cursor can go into the given inventory (equipment) slot
CursorHasItem()   - Returns true if the cursor currently holds an item
CursorHasMoney()   - true/false
CursorHasSpell()   - true/false
DeleteCursorItem()
DropCursorMoney - Drops the amount of money held by the cursor.
DropItemOnUnit("unit")   - Drops an item from the cursor onto a unit.
EquipCursorItem(invSlot)
GetCursorMoney - Returns the amount of money held by the cursor.
GetCursorPosition()   - Returns the cursor's position on the screen.
HideRepairCursor()
InRepairMode()   - Returns true if your cursor is in repair mode
PickupAction(slot)   - Drags an action out of the specified quickbar slot and holds it on the cursor.
PickupBagFromSlot(slot)   - Picks up the bag from the specified slot, placing it in the cursor. If an item is already picked up, this places the item into the specified slot, swapping the items if needed.
PickupContainerItem(bagID,slot)
PickupInventoryItem(invSlot)   - "Picks up" an item from the player's worn inventory.
PickupMacro(index)   - Pickup a macro button icon.
PickupMerchantItem(index)   - Places the item on the cursor.
PickupPetAction(slot)   - Drags an action from the specified pet action bar slot into the cursor.
PickupPlayerMoney - Picks up an amount of money from the player.
PickupSpell(spellID, "bookType")   - Loads an action button onto the cursor to be dropped into a quickbar slot.
PickupStablePet(index)   - ?.
PickupTradeMoney(amount)
PlaceAction(slot)   - Drops an action from the cursor into the specified quickbar slot.
PutItemInBackpack()   - attempts to place item in backpack (bag slot 0).
PutItemInBag(inventoryId)   - attempts to place item in a specific bag.
ResetCursor()
SetCursor("cursor" or nil)
ShowContainerSellCursor(index,slot)
ShowInspectCursor()   - Change the cursor to the magnifying glass inventory inspection cursor
ShowInventorySellCursor()   - ?.
ShowMerchantSellCursor(index)   - Changes the cursor to the merchant sell cursor.
ShowRepairCursor()
```

## Debugging Functions
```
debugprofilestart()   - starts a timer for profiling during debugging.
debugprofilestop()   - return the time in milliseconds since the last call to debugprofilestart()
FrameXML_Debug(flag)   - Sets FrameXML logging state which is output to /WoW Folder/Logs/FrameXML.log
GetDebugStats()
debugstack(start, count1, count2)   - Returns a string representation of the current calling stack (as of 1.9)
```

## Disabled Functions
These functions are present but have been disabled entirely.
```
AppendToFile - ?.
DeleteFile()   - ?
ReadFile()   - ?.
```

## Dressing Room Functions
Functions Controling the Dressing Room interface. NEW in 1700.
```
UI DressUpItem(itemId)   - Will show the DressingRoom UI with the given item ID equipped.
UI DressUpItemLink("itemString" or "itemLink")   - Will show the DressingRoom UI with the given item equipped.
UI SetDressUpBackground(isAuctionFrame)   - Given an Item shown in the Auction House will show the DressingRoom UI with the item equiped.
```

## Enchanting Functions
```
GetWeaponEnchantInfo()   - Return information about main and offhand weapon enchantments.
ReplaceEnchant()
ReplaceTradeEnchant()   - Confirm the replacement of an enchantment via trade.
BindEnchant()   - Confirm the binding of the item when enchanting.
```

## Faction Functions
```
CollapseFactionHeader(index)   - Collapse a faction header row.
ExpandFactionHeader(index)   - Expand a faction header row.
FactionToggleAtWar(index)   - Toggle the At War flag for a faction.
GetFactionInfo(index)   - Gets details for a specific faction/faction header.
GetNumFactions()   - Returns the number of lines in the faction display.
GetSelectedFaction()   - Returns the row index of the currently selected faction in reputation window. (New in 1.10)
GetWatchedFactionInfo()   - Returns information about the currently watched faction. (New in 1.10)
IsFactionInactive(index)   - Returns true if the faction is marked inactive. (New in 1.10)
SetFactionActive(index)   - Remove a faction from inactive group. (New in 1.10)
SetFactionInactive(index)   - Move a faction to inactive group. (New in 1.10)
SetSelectedFaction(index)   - Sets the currently selected faction in reputation window. (New in 1.10)
SetWatchedFactionIndex(index)   - Sets which faction should be watched in Blizzard reputation bar. (New in 1.10)
UnitFactionGroup("unit")   - Returns the faction group id and name of the specified unit. (eg. "Alliance")   - string returned is localization-independent (used in filepath)
```

## Frame Management
```
CreateFrame("frameType"[ ,"name"][, parent][, "inheritFrame"])   - Create a new frame of the specified type
CreateFont("name")   - Dynamically create a font object
GetNumFrames()   - Get the current number of Frame (and derivative) objects
EnumerateFrames(currentFrame)   - Get the Frame which follows currentFrame
GetMouseFocus()   - Returns the frame that currently has the mouse focus.
UI MouseIsOver - Determines whether or not the mouse is over the specified frame.
UI ToggleDropDownMenu(level, value, dropDownFrame, anchorName, xOffset, yOffset)
UI UIFrameFadeIn(frame, fadeTime, startAlpha, endAlpha)
UI UIFrameFlash(...)
```

## Friend Functions
```
AddFriend("playerName")   - Add a friend to your friend list.
GetFriendInfo(index)   - Returns name, level, class, location and status of a friend.
GetNumFriends()   - Returns how many friends are on your friend list.
GetSelectedFriend()   - Returns the index of the current selected friend.
RemoveFriend("name" or index)   - Removes a friend from your friend list
SetSelectedFriend(index)   - Update the current selected friend.
ShowFriends()   - Request updated friends information from server.
UI ToggleFriendsFrame([tabNumber])   - Opens/closes the friends pane (possibly on a specific tab).
```

## GM Functions
```
DeleteGMTicket()
GMRequestPlayerInfo()   - access denied (darn)
GetGMStatus()
GetGMTicket()
GetGMTicketCategories()   - Return all available ticket categories (not as a table)
GMSurveyAnswerSubmit(question, rank, comment)   - ?
GMSurveyCommentSubmit(comment)   - ?
GMSurveyQuestion ?
GMSurveySubmit ?
NewGMTicket(type,"text")
Stuck() - Informs the game engine that the player is Stuck.
UpdateGMTicket(type,"text")
```

## Gossip Functions
```
CloseGossip()   - Dismiss the gossip window.
GetGossipActiveQuests()   - Retrieves a list of the active (?) quests on the NPC you are talking to.
GetGossipAvailableQuests()   - Retrieves a list of the available (!) quests on the NPC you are talking to.
GetGossipOptions()   - Retrieves a list of the available gossip items on the NPC you are talking to.
GetGossipText()   - Retrieves the gossip text.
SelectGossipActiveQuest(index)   - Selects an active quest.
SelectGossipAvailableQuest(index)   - Selects an available quest.
SelectGossipOption(index)   - Selects on a gossip item.
```



## Group Functions
```
AcceptGroup()   - Accept the invitation to party.
CheckReadyCheckTime()   - Unknown, called from UIParent's OnUpdate!
ConfirmReadyCheck(isReady)   - Indicate if you are ready or not.
ConvertToRaid()   - Converts party to raid.
DeclineGroup()   - Decline the invitation to a party.
DoReadyCheck()   - Initiate a ready check.
GetLookingForGroup()
GetLootMethod()   - Return the currently active lootMethod
GetLootThreshold()   - Return the current loot threshold (for group/master loot)
GetMasterLootCandidate(index)   - Return the name of a player who is eligible to receive loot in master mode
GetNumPartyMembers()   - Returns the number of party members
GetPartyLeaderIndex()   - Returns the index of the party leader (1-4) if not yourself.
GetPartyMember(index)   - Returns the unit id of the party member at the given index if that party slot is filled, otherwise nil.
InviteByName("name")   - Invites the specified player to the group you are currently in.
InviteToParty("unit")   - Invite a unit to a party by its unit id (likely "target")
IsPartyLeader()   - Returns true if the player is the party leader.
LeaveParty()   - Quit the party
PromoteByName("name")   - Promotes by name the target.
PromoteToPartyLeader("unit")   - Promote a unit to party leader.
SetLookingForGroup(flag)
SetLootMethod("lootMethod"[, "masterPlayer" or threshold])   - Set the current loot method
SetLootThreshold(itemQuality)   - Set the threshold for group/master loot
UninviteByName("name")   - Uninvites (kicks) the named player from the current group if player is group leader.
UninviteFromParty("unit")   - Kick a unit from the party if player is group leader.
UnitInParty("unit")   - Returns true if the unit is a member of your party.
UnitIsPartyLeader("unit")   - Returns true if the unit is the leader of its party.
```

## Guild Functions
```
AcceptGuild()   - The player accepts the invitation to join a guild.
BuyGuildCharter("guildName")   - Purchases a guild charter for guildName.
CanEditGuildInfo()   - Returns true if you are allowed to edit the guild info
CanEditMOTD()   - Returns true if you are allowed to edit the guild motd.
CanEditOfficerNote()   - Returns true if you are allowed to edit a guild member's officer note.
CanEditPublicNote()   - Returns true if you are allowed to edit a guild member's public note.
CanGuildDemote()   - Returns true if you are allowed to demote a guild member.
CanGuildInvite()   - Returns true if you are allowed to invite a new member to the guild.
CanGuildPromote()   - ?.
CanGuildRemove()   - ?.
CanViewOfficerNote()   - ?.
CloseGuildRegistrar()   - ?.
CloseGuildRoster()   - ?.
CloseTabardCreation()
DeclineGuild()   - ?.
GetGuildCharterCost()   - Returns the cost of purchasing a guild charter.
GetGuildInfo("unit")   - This function returns the name of the guild unit belongs to.
GetGuildInfoText()   - Returns the persistant Guild Information data. (new in 1.9)
GetGuildRosterInfo(index)   - This function is used to get info on members in the guild.
GetGuildRosterLastOnline(index)   - Returns time since last online for indexth member in current sort order.
GetGuildRosterMOTD()   - Returns guild's MOTD.
GetGuildRosterSelection()   - Returns the index of the current selected guild member.
GetGuildRosterShowOffline()   - Returns true if showing offline members of the guild.
GetNumGuildMembers(offline)   - Returns the number of guild members total.
GetTabardCreationCost()   - Returns cost in coppers.
GetTabardInfo() -?.
GuildControlAddRank("name")   - Add another rank called "name". Only Guildmaster?
GuildControlDelRank - Delete rank? Only Guildmaster?
GuildControlGetNumRanks()   - Returns number of ranks after guild frame open. Any guild member can use this.
GuildControlGetRankFlags()   - Returns list of values for each permission for your rank.
GuildControlGetRankName(index)   - Returns name of the rank. Any guild member can use this.
GuildControlSaveRank("name")   - Only Guildmaster?
GuildControlSetRank(rank)   - ?.
GuildControlSetRankFlag(index, enabled)   - Enable/disable permission for some action.
GuildDemoteByName("name")   - ?.
GuildDisband()   - ?.
GuildInfo()   - Displays information about the guild you are a member of.
GuildInviteByName("name")   - ?.
GuildLeave()   - Removes you from your current guild.
GuildPromoteByName("name")   - ?.
GuildRoster()   - Fetches the guild list and fires a GUILD_ROSTER_UPDATE event.
GuildRosterSetOfficerNote(index, "note")   - ?.
GuildRosterSetPublicNote(index, "note")   - ?.
GuildSetLeaderByName("name")   - ?.
GuildSetMOTD("note")   - ?.
GuildUninviteByName("name")   - ?.
IsGuildLeader()   - ?.
IsInGuild()   - Lets you know whether you are in a guild.
SetGuildInfoText()   - Sets the persistant Guild Information data. Limit is 500 letters (GuildInfoEditBox is limited to this number). Longer texts are possible, but will be reseted during the day. (new in 1.9)
SetGuildRosterSelection(index)   - Selects/deselects a guild member according current sorting order.
SetGuildRosterShowOffline(enabled)   - Sets/Resets the show offline members flag.
SortGuildRoster("sort")   - Sorts guildroster according "sort". Any unknown values sort on "name".
TurnInGuildCharter()   - ?.
```

## Honor Functions
```
GetInspectHonorData()   - Return honor info for the inspected unit (if available).
GetInspectPVPRankProgress()   - Return rank progress for the inspected unit (if available). Ranges from 0 to 1.
GetPVPLastWeekStats()   - Get your PvP/Honor statistics for last week.
GetPVPLifetimeStats()   - Get your PvP/Honor statistics for your lifetime.
GetPVPRankInfo(rank[, unit])   - Get information about a specific PvP rank.
GetPVPRankProgress()   - Get information about the PvP rank progress.
GetPVPSessionStats()   - Get your PvP/Honor statistics for this session.
GetPVPThisWeekStats()   - Get your PvP/Honor statistics for this week.
GetPVPYesterdayStats()   - Get your PvP/Honor statistics for yesterday.
HasInspectHonorData()   - Determine if the inspected unit's honor data is available.
RequestInspectHonorData()   - Request honor data for inspected unit.
UnitIsCivilian("unit")   - Returns true if the unit is a civilian NPC.
UnitPVPName("unit")   - Returns unit's name with PvP rank prefix (e.g., "Corporal Allianceguy").
UnitPVPRank("unit")   - Get PvP rank information for requested unit.
```

## Ignore Functions
```
AddIgnore("name")   - Add a player to your ignore list.
AddOrDelIgnore("name")   - Toggles the ignore state of the specified name.
DelIgnore("name")   - Delete a player from your ignore list.
GetIgnoreName(index)   - Get the name of the player on your ignore list at index.
GetNumIgnores()   - Get the number of players on your ignore list.
GetSelectedIgnore()
SetSelectedIgnore(index)
```

## Inspection Functions
```
CheckInteractDistance("unit",distIndex)
ClearInspectPlayer()   - Reset inspect data once finished with it (Called on inspect window hide)
GetInspectHonorData()   - Return honor info for the inspected unit (if available).
GetInspectPVPRankProgress()   - Return rank progress for the inspected unit (if available). Ranges from 0 to 1.
HasInspectHonorData()   - Determine if the inspected unit's honor data is available.
UI InspectUnit("unit")   - Inspects the specified / selected "unit".
NotifyInspect("unit")
RequestInspectHonorData()   - Request honor data for inspected unit.
```

## Instance Functions
```
CanShowResetInstances()   - Determine if player can reset instances at the moment.
GetBattlefieldInstanceExpiration()   - Get shutdown timer for the battlefield instance.
GetBattlefieldInstanceInfo(index)   - Get the instance ID for a battlefield.
GetBattlefieldInstanceRunTime()   - In milliseconds, the time since battleground started. (seems to be queried from server because it is not in sync with time())
GetInstanceBootTimeRemaining()   - ?.
GetNumSavedInstances()   - Gets the number of instances that the player is saved to.
GetSavedInstanceInfo(index)   - Gets information about an instance that the player is saved to.
IsInInstance()   - Returns 1 if the player is in an instance.
ResetInstances()   - Confirm reset of instances.
```

## Inventory Functions
These functions manage your "inventory", that is, equipped items, as opposed to in nearly every other game where "inventory" refers to things you carry in your backpack.
```
AutoEquipCursorItem()   - Causes the equipment on the cursor to be equipped.
BankButtonIDToInvSlotID(buttonID)   - Returns the ID number of a bank button in terms of inventory slot ID.
CancelPendingEquip(index)   - This function is used to cancel a pending equip.
ConfirmBindOnUse()
ContainerIDToInventoryID(bagID)
CursorCanGoInSlot(invSlot)   - Return true if the item currently held by the cursor can go into the given inventory (equipment) slot
EquipCursorItem(invSlot)
EquipPendingItem(invSlot)   - Equips the currently pending Bind-on-Equip or Bind-on-Pickup item from the specified inventory slot. (Internal - do not use)
GetInventoryAlertStatus(index)   - Returns one of several codes describing the "status" of an equipped item.
GetInventoryItemBroken("unit",invSlot)   - Determine if an inventory item is broken (no durability).
GetInventoryItemCooldown("unit",invSlot)   - Get cooldown information for an inventory item.
GetInventoryItemCount("unit",invSlot)   - Determine the quantity of an item in an inventory slot.
GetInventoryItemLink("unit",invSlot)   - Returns an itemLink for an inventory (equipped) item.
GetInventoryItemQuality("unit",invSlot)   - Return the quality of an inventory item.
GetInventoryItemTexture("unit",invSlot)   - Return the texture for an inventory item.
GetInventorySlotInfo(invSlotName)   - Get the info for a named inventory slot (slot ID and texture)
GetWeaponEnchantInfo()   - Return information about main and offhand weapon enchantments.
HasWandEquipped()   - Returns 1 if a wand is equipped, false otherwise.
IsInventoryItemLocked(id)   - Returns whether an inventory item is locked, usually as it awaits pending action.
KeyRingButtonIDToInvSlotID(buttonID)   - Map a keyring button to an inventory slot button for use in inventory functions.
PickupBagFromSlot(slot)   - Picks up the bag from the specified slot, placing it in the cursor. If an item is already picked up, this places the item into the specified slot, swapping the items if needed.
PickupInventoryItem(invSlot)   - "Picks up" an item from the player's worn inventory.
SetInventoryPortaitTexture - ?.
UpdateInventoryAlertStatus()
UseInventoryItem(invSlot)   - Use an item in a specific inventory slot.
```

## Item Functions
These functions are those which operate on item links or item information directly.
```
GetAuctionItemLink("type", index)   - Returns an itemLink for the specified auction item.
GetContainerItemLink(bagID, slot)   - Returns the itemLink of the item located in bag#, slot#.
GetCraftItemLink(index)   - Returns an itemLink for the specified craftable item.
GetCraftReagentItemLink(index,reagentIndex)   - Returns an itemLink for one of the reagents needed to craft the given item
GetInventoryItemLink("unit",invSlot)   - Returns an itemLink for an inventory (equipped) item.
GetItemInfo(itemId or "itemString")   - Returns information about an item.
GetItemQualityColor(quality)   - Returns the RGB color codes for a quality.
GetMerchantItemLink(index)   - Returns an itemLink for the given purchasable item
GetQuestItemLink - Returns an itemLink for a quest reward item.
GetQuestLogItemLink - ?.
GetTradePlayerItemLink(id)   - Returns an itemLink for the given item in your side of the trade window (if open)
GetTradeSkillItemLink(index)   - Returns the itemLink for a trade skill item.
GetTradeSkillReagentItemLink(index, reagentId)   - Returns the itemLink for one of the reagents needed to craft the given item
GetTradeTargetItemLink(id)   - Returns an itemLink for the given item in the other player's side of the trade window (if open)
OffhandHasWeapon()   - Determine if your offhand carries a weapon.
UI SetItemRef(link, text, button)   - Handles item link tooltips in chat.
```

## Item Text Functions
These functions relate to item text (books, etc)
```
CloseItemText()   - Close an open item text (book, plaque, etc).
ItemTextGetCreator()   - Get the creator of the current text (if player-created).
ItemTextGetItem()   - Get the name of the text.
ItemTextGetMaterial()   - Get the material on which the text is printed.
ItemTextGetPage()   - Get the page number of the currently viewed page.
ItemTextGetText()   - Get the page contents of the currently viewed page.
ItemTextHasNextPage()   - Determine if there is another page after the current one.
ItemTextNextPage()   - Request the next page of the text.
ItemTextPrevPage()   - Request the previous page of the text.
```

## Key Binding Functions
```
GetBinding(index)   - Get action and key bindings for that index.
GetBindingAction("key")   - Get the action bound to that key.
GetBindingKey("command")   - Get the key(s) bound to that action.
UI GetBindingText("key", "prefix")   - Gets the string value for the key.
GetCurrentBindingSet()   - Queries if current set of key bindings is character or account specific
GetNumBindings()   - Get total number key bindings and headers.
LoadBindings(which)   - Loads default, account or character specific key binding set into memory from disk.
RunBinding("command"[, "up"])   - Executes the key binding named "command"
SaveBindings(which)   - Saves account or character specific key bindings from memory to disk.
SetBinding("key"[, "command"])   - Sets or unsets key bindings.
SetConsoleKey("key")   - Sets the console key (normally "`").
```

## Location Functions
These functions are related to the current location of the player and how it is displayed.
Globals associated with Location. Events associated with Location.
```
GetMinimapZoneText()   - Returns the zone text, that is displayed over the minimap.
GetRealZoneText()   - Returns either instance name or zone name
GetSubZoneText()   - Returns the subzone text (e.g. "The Canals").
GetZonePVPInfo()   - Returns PVP info for the current zone.
GetZoneText()   - Returns the zone text (e.g. "Stormwind City").
```

## Loot Functions
```
CloseLoot([uiFailedFlag])
ConfirmBindOnUse()
ConfirmLootRoll(slot)   - Confirm a loot roll (NEW IN 1300)
GetLootMethod()   - Return the currently active lootMethod
GetLootRollItemInfo(rollId)
GetLootRollItemLink(rollId)
GetLootRollTimeLeft(rollid)
GetLootSlotInfo(slot)   - Returns icon path, item name, and item quantity for the item in the given loot window slot
GetLootSlotLink(slot)   - Returns an itemLink for the item in the given loot window slot
GetLootThreshold()   - Return the current loot threshold (for group/master loot)
GetMasterLootCandidate(index)   - Return the name of a player who is eligible to receive loot in master mode
GetNumLootItems()   - Returns amount of objects to loot (number)
GiveMasterLoot(slot,index)
IsFishingLoot()
LootSlot(slot)   - Used to confirm the looting of a BOP item
LootSlotIsCoin(slot)
LootSlotIsItem(slot)
RollOnLoot(rollId[, roll])   - Roll or pass on a loot event started by the game engine.
SetLootMethod("lootMethod"[, "masterPlayer" or threshold])   - Set the current loot method
SetLootPortrait()
SetLootThreshold(itemQuality)   - Set the threshold for group/master loot
```

## Lottery Functions
```
BuyRandomPicks - ?   - Added in 1.12
CloseLottery - ?   - Added in 1.12
GetJackpotAmount - ?   - Added in 1.12
GetLastLotteryNumbers - ?   - Added in 1.12
GetLotteryPrizeInfo - ?   - Added in 1.12
GetMoneyPrizes - ?   - Added in 1.12
GetNextDrawTime - ?   - Added in 1.12
GetNumLotteryPrizes - ?   - Added in 1.12
GetNumPastDrawResults - ?   - Added in 1.12
GetPastDrawResult - ?   - Added in 1.12
SubmitNumbers - ?   - Added in 1.12
```

## Macro Functions
```
CreateMacro("name", icon, "body", local)   - Create a new macro.
DeleteMacro(index)   - Deletes a macro.
EditMacro(index, "name", iconIndex, "body", local)   - Saves a macro.
GetMacroIconInfo(index)   - Returns texture of the icons provided by Blizzard.
GetMacroIndexByName("name")   - Returns macro index.
GetMacroInfo(index)   - Returns "name", iconTextureID, "body", local.
GetNumMacroIcons()   - Returns the number of usable icons provided by Blizzard.
GetNumMacros()   - Returns the number of macros the user has.
PickupMacro(index)   - Pickup a macro button icon.
```

## Mail Functions
Events associated with Mail.
```
CheckInbox()   - Populate client's inbox with mail from server.
ClearSendMail()   - This clears the text in the send mail tab and places the COD item in the inventory. --Bug 15:52, 6 Feb 2005 (EST)
ClickSendMailItemButton()   - This seems to just simulate a click on the send item mail slot (will pickup the item there). --Bug 18:59, 4 Feb 2005 (EST)
CloseMail()   - Closes the mail window. --Bug 19:04, 4 Feb 2005 (EST)
DeleteInboxItem(index)   - Deletes the inbox item at index. It returns immediately, it does not seem to wait for the deletion to go through, giving the normal problems with rapid mail removal attempts.
DropCursorMoney - Drops the amount of money held by the cursor.
GetCoinIcon(amount)
GetInboxHeaderInfo(index)   - Returns information about a message in the inbox.
GetInboxItem(index)   - Returns description of the attachment attached to message at (index).
GetInboxNumItems()   - Returns the number of messages in your inbox.
GetInboxText(index)   - Returns the message text of message at (index). It also reads the inbox item, thus reducing its timeout to <= 3 days.
GetInboxInvoiceInfo(index)   - Returns informations about an auction house invoice. It also reads the inbox item, thus reducing its timeout to <= 3 days.
GetNumPackages()   - Not yet fully implemented. Currently it always returns 1. --Bug 16:28, 6 Feb 2005 (EST)
GetNumStationeries()   - Not yet fully implemented. Currently it always returns 1. --Mikk 17:03, 17 May 2006 (EDT)
GetPackageInfo(index)   - Not yet fully implemented. Currently an index of 1 returns "Test Package". --Bug 16:28, 6 Feb 2005 (EST)
GetSelectedStationeryTexture()   - Not yet fully implemented. Currently it returns "STATIONERYTEST" when the mailbox is open. --Bug 16:28, 6 Feb 2005 (EST)
GetSendMailCOD()   - ?.
GetSendMailItem()   - ?.
GetSendMailMoney()   - ?.
GetSendMailPrice()   - ?.
GetStationeryInfo(index)   - Not yet fully implemented. Currently an index of 1 returns "Default Stationery". --Mikk 17:03, 17 May 2006 (EDT)
HasNewMail()   - Returns nil if there is no new mail. --Bug 19:14, 4 Feb 2005 (EST)
InboxItemCanDelete(index)   - ?.
ReturnInboxItem(index)   - Returns to the sender the attached item in the mail message at the specified index.
SelectPackage(index)   - Not yet fully implemented. It does nothing visible. --Bug 16:28, 6 Feb 2005 (EST)
SelectStationery(index)   - Not yet fully implemented. It does nothing visible. --Bug 16:28, 6 Feb 2005 (EST)
SendMail("target", "subject", "body")   - If the mailbox is open, this sends mail. --Buttahcup 4 Feb 2005
SetSendMailCOD(amount)   - Make next mail sent using SendMail() COD target for amount. --Drundia 21:30, 25 April 2006 (EDT)
SetSendMailMoney(amount)   - Add money to next mail sent using SendMail(). --Drundia 21:30, 25 April 2006 (EDT)
TakeInboxItem(index)   - Take the attached item from the mailbox message at index.
TakeInboxMoney(index)   - Take the attached money from the mailbox message at index. --Drundia 21:30, 25 April 2006 (EDT)
TakeInboxTextItem(index)   - Creates a permanent copy of letter (readable "Plain Letter") --Drundia 21:30, 25 April 2006 (EDT).
```

## Mapping Functions
These functions are related to display of the world map.
```
GetCorpseMapPosition()   - Returns the position of the corpse on the current world map.
GetCurrentMapContinent()   - Returns the number of the continent the world map is currently showing.
GetCurrentMapZone()   - Returns the number of the zone the world map is currently showing.
GetMapContinents()   - Returns the continent names.
GetMapInfo()   - Returns the name and size of the current world map.
GetMapLandmarkInfo(landmarkIndex)   - Returns information about a landmark on the current world map.
GetMapOverlayInfo(overlayIndex)   - Returns information about an overlay on the current world map.
GetMapZones(continentIndex)   - Returns the zone names of a continent.
GetNumMapLandmarks()   - Returns the number of landmarks on the current world map.
GetNumMapOverlays()   - Returns the number of overlays on the current world map.
GetPlayerMapPosition("unit")   - Returns the position of a unit on the current world map.
GetWorldLocMapPosition(continent, x, y)
ProcessMapClick(x,y)   - Passes a click to the client, which then calculates if the zone has to be changed.
RequestBattlefieldPositions()   - Request new data for GetBattlefieldPosition().
SetMapToCurrentZone()   - Sets the current world map to the zone the player is presently in.
SetMapZoom(continentIndex[, zoneIndex])   - Sets the current world map to a specific continent and optionally zone.
SetupFullscreenScale()   - Configures scale of full-screen views, such as the world map, to best fill screen.
UI ToggleMinimap - Turns the minimap display on/off.
UI ToggleWorldMap - Turns the world map on/off.
UpdateMapHighlight(x,y)   - Provides map rollover information for highlighting.
CreateWorldMapArrowFrame("frame")   - create a arrow cursor for the player position and orientation.
UpdateWorldMapArrowFrames()   - update the orientation of the arrow cursor based on the current player orientation.
ShowWorldMapArrowFrame(bool)   - show or hide the arrow representing the player.
PositionWorldMapArrowFrame(x,y)   - set the position of the arrow representing the player
```

## Meeting Stone Functions
```
CancelMeetingStoneRequest()   - Remove character from an instance's Meeting Stone queue
GetMeetingStoneStatusText()
IsInMeetingStoneQueue()
```

## Merchant Functions
```
BuyMerchantItem(index[, qty])   - Buys an item from a merchant.
BuybackItem(index)   - Buys back a sold item.
CanMerchantRepair()   - Returns true if the merchant can repair items.
CloseMerchant()   - Closes the merchant window.
GetBuybackItemInfo(index)   - Returns information about a buyback item.
GetMerchantItemInfo(index)   - Returns information about the given purchasable item
GetMerchantItemLink(index)   - Returns an itemLink for the given purchasable item
GetMerchantItemMaxStack(index)   - Returns the maximum number of items in a stack.
GetMerchantNumItems()   - Returns the number of items the merchant sells.
GetRepairAllCost()
HideRepairCursor()
InRepairMode()   - Returns true if your cursor is in repair mode
IsVendorActive - ?   - Added in 1.12
PickupMerchantItem(index)   - Places the item on the cursor.
RepairAllItems()
ShowMerchantSellCursor(index)   - Changes the cursor to the merchant sell cursor.
ShowRepairCursor()
```

## Movement Functions
Use with caution - movement started by a script must be stopped by script. Keys/Mouse will not stop movement. These functions no longer work (fail silently) in patch 1.6 if NOT triggered from a hardware event (just like spell casts). As of patch 1.10 many of these functions were protected for use of only Blizzard signed code.
```
PROTECTED CameraOrSelectOrMoveStart()   - Begin "Left click" in the 3D world. (1.10 - Protected)
PROTECTED CameraOrSelectOrMoveStop([stickyFlag])   - End "Left click" in the 3D world. (1.10 - Protected)
FollowByName("name"[, exactMatch])   - Follow a player with the specified player name
FollowUnit("unit")   - Follow an ally with the specified UnitID
PROTECTED Jump()   - The player jumps.
PROTECTED MoveBackwardStart - The player begins moving backward at the specified time.
PROTECTED MoveBackwardStop - The player stops moving backward at the specified time.
PROTECTED MoveForwardStart - The player begins moving forward at the specified time.
PROTECTED MoveForwardStop - The player stops moving forward at the specified time.
PROTECTED StrafeLeftStart - The player begins strafing left at the specified time.
PROTECTED StrafeLeftStop - The player stops strafing left at the specified time.
PROTECTED StrafeRightStart - The player begins strafing right at the specified time.
PROTECTED StrafeRightStop - The player stops strafing right at the specified time.
PROTECTED ToggleAutoRun - Turns auto-run on or off
ToggleMouseMove()
PROTECTED ToggleRun - Toggle between running and walking.
PROTECTED TurnLeftStart - The player starts turning left at the specified time.
PROTECTED TurnLeftStop - The player stops turning left at the specified time.
PROTECTED TurnOrActionStart()   - Begin "Right Click" in the 3D world. (1.10 - Protected)
PROTECTED TurnOrActionStop()   - End "Right Click" in the 3D world. (1.10 - Protected)
PROTECTED TurnRightStart - The player starts turning right at the specified time.
PROTECTED TurnRightStop - The player stops turning right at the specified time.
```

## Music Player Functions
These are for Mac iTunes only
```
MusicPlayer_BackTrack() - Go back a track (Mac iTunes only)   - Added in 1.12
MusicPlayer_NextTrack() - Go forward a track (Mac iTunes only)   - Added in 1.12
MusicPlayer_PlayPause() - Toggle play/paulse (Mac iTunes only)   - Added in 1.12
MusicPlayer_VolumeDown() - Reduce music volume (Mac iTunes only)   - Added in 1.12
MusicPlayer_VolumeUp() - Increase music volume (Mac iTunes only)   - Added in 1.12
```

## Pet Functions
```
BuyStableSlot()
CastPetAction(index)   - Cast the corresponding pet skill.
CheckPetUntrainerDist()   - Check wether the player is close enough to the pet untrainer.
ClickStablePet(index)   - ?.
ClosePetStables()   - Close the pet stables user interface.
ConfirmPetUnlearn()   - Confirm the request for unlearning pet abilities
DropItemOnUnit("unit")   - Drops an item from the cursor onto a unit.
GetNextStableSlotCost()
GetNumStablePets()   - Returns the number of pets in the stable.
GetNumStableSlots()   - Returns the number of stable slots you own.
GetPetActionCooldown(index)   - Returns cooldown information for the pet action at the specificed pet action bar slot.
GetPetActionInfo(index)   - Returns information on the pet action at the specified pet action bar slot.
GetPetActionsUsable()   - Returns a value indicating if the player's pet's actions can be used at this time.
GetPetExperience()   - Returns the pet's current xp, and total xp required for next level.
GetPetFoodTypes()   - Returns a list of the food types the player's pet can eat.
GetPetHappiness()   - Returns the pet's happiness, damage percentage, and loyalty gain rate.
GetPetIcon()   - Returns the path to the texture to use as the icon for the player's pet.
GetPetLoyalty()   - Returns the name of the pet's current loyalty level.
GetPetTimeRemaining()   - Returns in milliseconds about some timeout for the player's pet.
GetPetTrainingPoints()   - Returns the pet's current total and used training points.
GetSelectedStablePet()   - ?.
GetStablePetFoodTypes(index)   - Returns a list of the food types a specific stabled pet can eat.
GetStablePetInfo(index)   - Returns information about a specific stabled pet.
HasPetSpells()   - Returns true if the player has pet spells.
HasPetUI()   - Returns true if the player has a pet User Interface.
PetAbandon()   - Permanently abandons your pet.
PetAggressiveMode()   - Set your pet in aggressive mode.
PetAttack()   - Instruct your pet to attack your target.
IsPetAttackActive()   - Returns true if the pet is currently attacking.
PetStopAttack()   - Stop the attack of the pet.
PetCanBeAbandoned()   - Returns true if the pet is abandonable.
PetCanBeRenamed()   - Returns true if the pet can be renamed.
PetDefensiveMode()   - Set your pet in defensive mode.
PetDismiss()   - Dismiss your pet.
PetFollow()   - Instruct your pet to follow you.
PetHasActionBar()   - Determine if player has a pet with an action bar.
PetPassiveMode()   - Set your pet into passive mode.
PetRename("name")   - Renames the pet.
PetWait()   - Instruct your pet to remain still.
PickupPetAction(slot)   - Drags an action from the specified pet action bar slot into the cursor.
PickupStablePet(index)   - ?.
SetPetStablePaperdoll(modelObject)   - ?.
StablePet(index)   - ?.
TogglePetAutocast(index)   - Toggles whether the specified pet ability should autocast or not.
ToggleSpellAutocast(index, bookIndex)   - Toggles whether the specified pet ability should autocast or not. (in the spellbook).
GetSpellAutocast(index, bookIndex)   - Check wether the specified pet ability autocasts or not.
UnstablePet(index)   - ?
```

## Petition Functions
```
CanSignPetition()   - ?.
ClosePetition()   - ?.
GetNumPetitionNames()   - ?.
GetPetitionInfo()   - ?.
GetPetitionNameInfo(index)   - ?.
OfferPetition()   - ?.
RenamePetition("name")   - ? - (NEW IN 1300)
SignPetition()   - ?.
```

## Quest Functions
```
AbandonQuest - Abandon the specified quest.
AcceptQuest - Accept the specified quest.
AddQuestWatch(x)   - Add a quest to the watch list.
CloseQuest - ?.
CollapseQuestHeader - Collapses a quest header.
CompleteQuest - Complete the specified quest.
ConfirmAcceptQuest - Accept the quest. Yes. Really accept it.
DeclineQuest - Declines the currently offered quest.
ExpandQuestHeader - Expands a quest header.
GetAbandonQuestName - Gets the name of a quest while it is being abandoned.
GetActiveLevel(index) - Gets the level of an active quest (only available after QUEST_GREETING event).
GetActiveTitle(index) - Gets the title of an active quest (only available after QUEST_GREETING event).
GetAvailableLevel(index) - Gets the level of an available quest (only available after QUEST_GREETING event).
GetAvailableTitle(index) - Gets the title of an available quest (only available after QUEST_GREETING event).
GetGreetingText()
GetNumActiveQuests - Gets the number of currently active quests from this NPC (only available after QUEST_GREETING event).
GetNumAvailableQuests - Gets the number of currently available quests from this NPC (only available after QUEST_GREETING event).
GetNumQuestChoices - Returns the number of rewards for a completed quest.
GetNumQuestItems - Returns the number of items nessecary to complete a particular quest.
GetNumQuestLeaderBoards([questIndex])   - Returns the number of available quest objectives.
GetNumQuestLogChoices - Returns the number of options someone has when getting a quest item.
GetNumQuestLogEntries - Returns the number of entries in the quest log.
GetNumQuestLogRewards - Returns the count of the rewards for a particular quest.
GetNumQuestRewards - ?.
GetNumQuestWatches()   - Returns the number of quest watches active.
GetObjectiveText()   - Gets the objective of the current quest.
GetProgressText()
GetQuestBackgroundMaterial - Returns the material string associated with the particular quest.
GetQuestGreenRange()   - Return for how many levels below you quests and mobs remain "green" (i.e. yield xp)
GetQuestIndexForTimer - ?.
GetQuestIndexForWatch(watchIndx)   - Return the quest index for the specified watch
GetQuestItemInfo - Returns basic information about the quest items.
GetQuestItemLink - Returns an itemLink for a quest reward item.
GetQuestLogChoiceInfo - Returns a bunch of data about a quest reward choice from the quest log.
GetQuestLogItemLink - ?.
GetQuestLogLeaderBoard(ldrIndex[, questIndex])   - Gets information about the objectives for a quest.
GetQuestLogPushable - Returns true if the currently loaded quest in the quest window can be shared.
GetQuestLogQuestText - Returns the description and objectives required for the specified quest.
GetQuestLogRequiredMoney - ?.
GetQuestLogRewardInfo - Returns a pile of reward item info.
GetQuestLogRewardMoney - Returns a number representing the amount of copper returned by a particular quest.
GetQuestLogRewardSpell - ?.
GetQuestLogSelection - Returns a number associated with the QuestLogSelection index.
GetQuestLogTimeLeft - ?.
GetQuestLogTitle - Returns the string which is associated with the specific QuestLog Title in the game.
GetQuestMoneyToGet - ?
GetQuestReward - Gets the quest reward specified.
GetQuestText - Gets the description of the current quest.
GetQuestTimers - Returns all of the quest timers currently in progress.
GetRewardMoney - Returns a number representing the amount of copper returned by a particular quest.
GetRewardSpell - ?.
GetRewardText - ?.
GetTitleText - Retrieves the title of the quest while talking to the NPC about it.
IsCurrentQuestFailed - ?.
IsQuestCompletable - Returns true if a quest is possible to complete.
IsQuestWatched(questIndex)   - Determine if the specified quest is watched.
IsUnitOnQuest(questIndex, "unit")   - Determine if the specified unit is on the given quest.
QuestChooseRewardError - Throws an error when the quest choose reward method doesn't work.
QuestLogPushQuest - Initiates the sharing of the currently viewed quest in the quest log.
RemoveQuestWatch(index)   - Remove a quest watch (Is the index a quest or watch index?).
SelectQuestLogEntry - ?.
SetAbandonQuest - Called before AbandonQuest.
UI ToggleQuestLog - Opens/closes the quest log.
```

## Raid Functions
```
ConvertToRaid()   - Converts party to raid.
DemoteAssistant("name")   - Demotes player from assistant status. Requires raid leadership.
GetNumRaidMembers()   - Returns the number of raid members.
GetRaidRosterInfo(index)   - Returns information about the members of your raid .
GetRaidRosterSelection - ?.
GetRaidTargetIndex("unit")   - Get the raid target index assigned to a unit.
IsRaidLeader()   - Returns a value based on whether the player is a raid leader
IsRaidOfficer()   - Returns a value based on whether the player is a raid officer (assistant (?)).
PromoteToAssistant("name")   - Promotes player to assistant status. Requires raid leadership.
RequestRaidInfo()   - Returns information about which instances you are saved to
SetRaidRosterSelection(index)   - ?.
SetRaidSubgroup(index, subgroup)   - Move a raid member from his current subgroup into a different (non-full) subgroup.
SwapRaidSubgroup(index1, index2)   - Swaps raid members into different groups
SetRaidTarget("unit", index)   - Set the raid target index for a unit.
UninviteFromRaid(index)   - Boots someone from a raid
UnitInRaid("unit")   - Returns 1 if unit is in your raid, nil if not.
```

## Settings Functions
```
GetBaseMip()   - Get the world appearance Texture Detail.
GetCVar("varname")   - Get the current (active) setting for a variable in config.wtf
GetCVarDefault("varname")
GetCurrentMultisampleFormat()   - Get the current in-use multi-sample (antialias) format.
GetCurrentResolution()   - Get the index of the current screen resolution.
GetDoodadAnim()   - ???
GetFarclip()   - Get the world appearance Terrain Distance.
GetGamma()
GetMultisampleFormats()   - Get the available multi-sample (antialias) formats..
GetRefreshRates(x)
GetScreenResolutions()
GetTerrainMip()   - Get the world appearance Terrain Texture.
GetTexLodBias()
GetVideoCaps()
GetWaterDetail()
GetWorldDetail()   - Get the world appearance Environment Detail.
HideFriendNameplates()   - Turn off display of nameplates above friendly units.   - Added in 1.12
HideNameplates()   - Turn off display of nameplates.
RegisterCVar("varname"[, value]) - Registers a variable for use with the GetCVar and SetCVar functions.
ResetPerformanceValues()
ResetTutorials()
SetBaseMip(value)   - Set the world appearance Texture Detail (0,1).
SetCVar("cvar", value[, "scriptCVar"])   - Set the value of a variable in config.wtf
SetDoodadAnim()   - ?.
SetEuropeanNumbers(flag)   - Sets the decimal separator to a comma instead of a dot
SetFarclip(value)   - Set the world appearance Terrain Distance (177-777).
SetGamma(value)
SetLayoutMode()
SetMultisampleFormat(index)   - Set the multi-sample (antialias) format to use.
SetScreenResolution(x)
SetTerrainMip(value)   - Set the world appearance Terrain Texture (0,1).
SetTexLodBias()
SetWaterDetail()
SetWorldDetail(value)   - Set the world appearance Environment Detail (0,1,2).
ShowCloak(flag)   - Set whether player's cloak is displayed.
ShowFriendNameplates()   - Turn on display of nameplates above friendly units.   - Added in 1.12
ShowHelm(flag)   - Set whether player's helm is displayed.
ShowNameplates()   - Turn on display of nameplates.
ShowingCloak()   - Return 1 if player's cloak is displayed, nil otherwise.
ShowingHelm()   - Return 1 if player's helm is displayed, nil otherwise.
ToggleCollision()
ToggleCollisionDisplay()
TogglePerformanceDisplay()
TogglePerformanceValues()
TogglePlayerBounds()
TogglePortals()
ToggleTris()
TutorialsEnabled()
```

## Skill Functions
```
CollapseSkillHeader(index)
ExpandSkillHeader(index)
GetAdjustedSkillPoints()
GetNumSkillLines()   - get the number of lines in the skill window, including headers
GetSelectedSkill()
GetSkillLineInfo(index)   - get the information for a selected skill
```

## Spell Functions
spellID is the index of a spell in a spellbook. The indices increase from top to bottom, then left to right, then between categories (e.g.: General -> Discipline). spellIDs will change as players learn new spells and professions.
```
CastShapeshiftForm(index)
CastSpell(spellID, "bookType")   - Cast the specified spell by ID. spellbookTab is "spell" or "pet".
CastSpellByName("name"[, onSelf])   - Cast the specified spell by display name.
GetCraftSpellFocus(index)   - ?.
GetNumShapeshiftForms()
GetNumSpellTabs()   - Returns the total number of tabs in the user's spellbook.
GetQuestLogRewardSpell - ?.
GetRewardSpell - ?.
GetShapeshiftFormCooldown(index)
GetShapeshiftFormInfo(index)   - Retrieves information about an available ShapeshiftForm or Stance.
GetSpellCooldown(spellID, "bookType")   - Retrieves data on the cooldown of a specific spell within your spellbook..
GetSpellName(spellID, "bookType")   - Returns the spell name and spell rank for a spell in the player's spellbook.
GetSpellTabInfo(spellbookTabNum)   - Returns information about the specified spellbook tab.
GetSpellTexture(spellID, "bookType")   - ?.
GetTrackingTexture()   - Return the texture of the current tracking buff, if one is active.
IsCurrentCast(id, "bookType")
IsSpellPassive(spellID, "bookType")   - Returns whether the icon in your spellbook is a Passive ability.
IsTrainerServiceLearnSpell(index)
PickupSpell(spellID, "bookType")   - Loads an action button onto the cursor to be dropped into a quickbar slot.
PlayerHasSpells()   - ?.
SpellCanTargetUnit("unit")   - Returns true if the spell awaiting target selection can be cast on the specified unit.
SpellIsTargeting()   - Returns true if a spell has been cast and is awaiting target selection.
SpellStopCasting()   - Stops the current spellcast. (As of 1.10 PTR, this function must be used in direct response to a hardware input event, such as a mouse click or key press.)
SpellStopTargeting()   - Cancels the spell awaiting target selection.
SpellTargetUnit("unit")   - Casts the spell awaiting target selection on the specified unit.
UI ToggleSpellBook("bookType")   - Shows the spellbook. Can show your spells or your pet's.
UpdateSpells()   - ?.
```

## System Functions
```
ConsoleExec("command")   - Execute a console command.
GetBuildInfo()   - Returns information about current client build.
GetFramerate()   - Returns the current framerate (full precision)
GetGameTime - Returns the time in-game.
GetLocale()   - Returns client locale, example 'enUS'.
GetCursorPosition()   - Returns the cursor's position on the screen.
GetNetStats()   - Get bandwidth and latency network information.
GetRealmName()   - returns the name of the server a user is logged in to
GetScreenHeight()   - Returns the height of the window in pixels.
GetScreenWidth()   - Returns the width of the window in pixels.
UI GetText()   - Used to localize some client text.
GetTime()   - Returns the system uptime in seconds (millisecond precision).
InCinematic()
IsAltKeyDown()   - Returns true if the alt key is currently depressed.
IsControlKeyDown()   - Returns true if the control key is currently depressed.
IsLinuxClient()   - Boolean - Returns true if WoW is being run on Linux
IsMacClient()   - Checks client system
IsShiftKeyDown()   - Returns true if the shift key is currently depressed.
IsWindowsClient - ?.
OpeningCinematic()   - shows the opening movie for a player's race
PlayMusic()   - Plays the specified mp3.
PlaySound()   - Plays the specified built-in sound effect.
PlaySoundFile()   - Plays the specified sound file.
ReloadUI()   - Reloads the UI from source files
RepopMe()   - The "Release Spirit" button. Sends you to the graveyard when dead. -Moof
RequestTimePlayed()   - Request a summary of time played from the server.
RestartGx()   - Restarts the graphical engine. Needed for things such as resolution changes to take effect.
RunScript("script")   - Execute "script" as a block of LUA code.
Screenshot()   - Takes a screenshot.
UI SecondsToTime - Converts a number of seconds into a readable days / hours / etc. formatted string.
StopCinematic()
StopMusic()   - Stops the currently playing mp3.
UI UIParentLoadAddOn("AddOnName")   - Loads or Reloads the specified AddOn, and pops up an error message if it fails to load for any reason.
UI TakeScreenshot()   - Takes a screenshot.
UI _ERRORMESSAGE(value)   - Displays the script error dialog with optional text
debuginfo()   - Output win32 debug text. Freeware debug message viewer: DebugView (Has no effect on live server)
getglobal("object")   - Given an object name will return the object itself.
UI message("text")   - Displays a message box with your text message and an "Okay" button.
setglobal("object", value)   - set the global "object" to the given value.
```

## Talent Functions
```
BuyTrainerService(index)   - Used for buying new/upgrading professions, profession items and class skills.
CheckTalentMasterDist()
ConfirmTalentWipe()
GetNumTalentTabs()   - return number of talent trees (usually 3)
GetNumTalents(tabIndex)   - return number of talents in tree
GetTalentInfo(tabIndex,talentIndex)   - return name, iconTexture, tier, column, rank, maxRank, isExceptional, meetsPrereq
GetTalentPrereqs(tabIndex,talentIndex)   - return tier, column, isLearnable
GetTalentTabInfo(tabIndex)   - return name, iconTexture, pointsSpent, background
IsTalentTrainer - ?.
LearnTalent(tabIndex,talentIndex)
```

## Targetting Functions
```
AssistByName("playername")   - Assists the player whose name is entered.
AssistUnit("unit")   - Instructs your character to assist the specified unit.
AttackTarget()   - Attacks the targetted unit.
ClearTarget()   - Clears the selected target.
ClickTargetTradeButton(index)
TargetByName("name"[, exactMatch])   - Selects the specified player as the current target.
TargetLastEnemy()   - Selects the last targetted enemy as the current target.
TargetLastTarget()   - Selects the last target as the current target.
TargetNearestEnemy([reverseFlag])   - Selects the nearest enemy as the current target.
TargetNearestFriend()   - Selects the nearest friendly unit as the current target.
TargetNearestPartyMember()   - Selects the nearest Party member as the current target.
TargetNearestRaidMember - Selects the nearest Raid member as the current target.
TargetUnit("unit")   - Selects the specified unit as the current target.
```

## Taxi Functions
```
CloseTaxiMap()   - Closes the Flightpath Map.
NumTaxiNodes()   - Returns the number of nodes (flight paths) on an open taxi map.
SetTaxiMap(frame)   - ?.
TakeTaxiNode(slot)   - Takes the named taxi node.
TaxiNodeCost(slot)   - Returns the cost in copper of a node.
TaxiNodeGetType(slot)   - Returns the status of a node.
TaxiGetSrcX(slot, hop)   - ?.
TaxiGetSrcY(slot, hop)   - ?.
TaxiGetDestX(slot, hop)   - ?.
TaxiGetDestY(slot, hop)   - ?.
TaxiNodeSetCurrent(slot)   - Renumbers slots based on new current slot.
TaxiNodeName(slot)   - Returns the name of a node.
TaxiNodePosition(slot)   - Returns position (x,y) of node on the map.
UnitOnTaxi("unit")   - Returns 1 if unit is on a taxi.
```

## Toggle Functions
```
UI ToggleBackpack()   - Toggles your backpack open/closed.
UI ToggleBag(bagID)   - Opens or closes the specified bag.
UI ToggleCharacter(index)   - Toggles the character pane to the specified frame.
UI ToggleCombatLog - Opens/closes the combat log.
UI ToggleFramerate - Show/Hide the FPS.
UI ToggleFriendsFrame([tabNumber])   - Opens/closes the friends pane (possibly on a specific tab).
UI ToggleGameMenu - Opens/closes the game menu.
UI ToggleHelpFrame - Opens the Help Request frame.
UI ToggleKeyRing - Opens/closes the key ring.
UI ToggleMinimap - Turns the minimap display on/off.
UI ToggleQuestLog - Opens/closes the quest log.
UI ToggleSpellBook("bookType")   - Shows the spellbook. Can show your spells or your pet's.
UI ToggleTalentFrame - Opens the Talent frame.
UI ToggleWorldMap - Turns the world map on/off.
```

## TradeSkill Functions
```
CloseTradeSkill()   - Closes an open trade skill window.
CollapseTradeSkillSubClass(index)   - Collapses the specified subclass header row.
DoTradeSkill(index[, repeatTimes])   - Performs the tradeskill a specified # of times.
ExpandTradeSkillSubClass(index)   - Expands the specified subclass header row.
GetFirstTradeSkill()   - Returns the index of the first non-header trade skill entry.
GetNumTradeSkills()   - Get the number of trade skill entries (including headers).
GetTradeSkillCooldown(index)   - Returns the number of seconds left for a skill to cooldown.
GetTradeSkillIcon(index)   - Returns the texture name of a tradeskill's icon.
GetTradeSkillInfo(index)   - Retrieves information about a specific trade skill.
GetTradeSkillInvSlotFilter(slotIndex)   - Returns 1 if items corresponding to slotIndex are currently visible, otherwise nil.
GetTradeSkillInvSlots()   - Returns a list of the available inventory slot types.
GetTradeSkillItemLink(index)   - Returns the itemLink for a trade skill item.
GetTradeSkillItemStats(index)   - Returns information about the item produced.
GetTradeSkillLine()   - Returns information about the selected skill line.
GetTradeSkillNumMade(index)   - Gets the number of items made in a single use of a skill.
GetTradeSkillNumReagents(tradeSkillRecipeId)   - Returns the number of different reagents required.
GetTradeSkillReagentInfo(tradeSkillRecipeId, reagentId)   - Returns data on the reagent, including a count of the player's inventory.
GetTradeSkillReagentItemLink(index, reagentId)   - Returns the itemLink for one of the reagents needed to craft the given item
GetTradeSkillSelectionIndex()   - Returns the Id of the currently selected trade skill, 0 if none selected.
GetTradeSkillSubClassFilter(filterIndex)   - Returns 1 if items corresponding to filterIndex are currently visible, otherwise nil.
GetTradeSkillSubClasses()   - Returns a list of the valid subclasses.
GetTradeSkillTools(index)   - Returns information about the tools needed for a tradeskill.
GetTradeskillRepeatCount()   - ?.
IsTradeskillTrainer()   - Returns 1 if trainer is for a tradeskill.
IsTrainerServiceTradeSkill()   - ?.
SelectTradeSkill(index)   - Select a specific trade skill in the list.
SetTradeSkillInvSlotFilter(slotIndex, onOff[, exclusive] )   - Set the inventory slot type filter.
SetTradeSkillSubClassFilter(slotIndex, onOff[,exclusive] )   - Set the subclass filter.
```

## Trading Functions
```
AcceptTrade()   - A pending trade will be accepted.
AddTradeMoney()   - Adds the money dropped into the player's trade frame.
BeginTrade()   - Begins the trade with the target.
CancelTrade()   - Declines the offer to trade with the other player.
CancelTradeAccept - Cancels the trade attempt which required an accept.
ClickTargetTradeButton(index)
ClickTradeButton(index)   - Equivalent of a mouseclick on the trade window buttons [1-7]
CloseTrade()   - Closes the trade.
GetPlayerTradeMoney - Returns the amount of money the player has in the trade window.
GetTargetTradeMoney - Returns the amount of money in the trade frame of the target player.
GetTradePlayerItemInfo(id)   - Returns information about a trade item.
GetTradePlayerItemLink(id)   - Returns an itemLink for the given item in your side of the trade window (if open)
GetTradeTargetItemInfo(id)   - Returns information about a trade item.
GetTradeTargetItemLink(id)   - Returns an itemLink for the given item in the other player's side of the trade window (if open)
InitiateTrade(UnitId)   - Asks the specified unit to trade.
PickupPlayerMoney - Picks up an amount of money from the player.
PickupTradeMoney(amount)
ReplaceTradeEnchant()   - Confirm the replacement of an enchantment via trade.
SetTradeMoney(amount)
```

## Training Functions
```
BuyTrainerService(index)   - Used for buying new/upgrading professions, profession items and class skills.
CloseTrainer()   - Closes the trainer window.
CollapseTrainerSkillLine(index)   - Collapses a header, hiding all spells below it.
ExpandTrainerSkillLine(index)   - Expands a header, showing all spells below it.
GetNumTrainerServices()   - Get the number of the trainer services.
GetTrainerGreetingText()   - Get the trainer's greeting text.
GetTrainerSelectionIndex()   - Get the index of the selected trainer service.
GetTrainerServiceAbilityReq(trainerIndex,reqIndex)   - Used for displaying the requirements to learn a new profession, profession skill or class skill.
GetTrainerServiceCost(index)   - Returns the cost of a specific trainer service.
GetTrainerServiceDescription(index)   - Returns the description of a specific trainer service.
GetTrainerServiceIcon(index)   - Returns icon texture for a trainer service.
GetTrainerServiceInfo(index)   - Returns information about a trainer service.
GetTrainerServiceLevelReq(index)   - Get the required level to learn the skill.
GetTrainerServiceNumAbilityReq - Get the maximum number of requirements that GetTrainerServiceAbilityReq() has.
GetTrainerServiceSkillLine - ?.
GetTrainerServiceSkillReq(index)   - Returns a String and Variable for the requirements of a specific trainer service.
GetTrainerServiceStepIncrease()   - ?.
GetTrainerServiceStepReq - ?.
GetTrainerServiceTypeFilter("filter")   - Returns the status of a skill filter in the trainer window.
GetTrainerSkillLineFilter()   - ?;
GetTrainerSkillLines()   - ?;
IsTalentTrainer - ?.
IsTradeskillTrainer()   - Returns 1 if trainer is for a tradeskill.
IsTrainerServiceLearnSpell(index)
IsTrainerServiceSkillStep()   - ?.
IsTrainerServiceTradeSkill()   - ?.
OpenTrainer()   - ?.
SelectTrainerService - ?.
SetTrainerServiceTypeFilter("filter",state)   - Sets the status of a skill filter in the trainer window.
SetTrainerSkillLineFilter()   - ?.
```

## Unit Functions
These are functions which act on one or more units. Units are identified by UnitIds.
```
AssistUnit("unit")   - Instructs your character to assist the specified unit.
CheckInteractDistance("unit",distIndex)
DropItemOnUnit("unit")   - Drops an item from the cursor onto a unit.
FollowUnit("unit")   - Follow an ally with the specified UnitID
InviteToParty("unit")   - Invite a unit to a party by its unit id (likely "target")
IsUnitOnQuest(questIndex, "unit")   - Determine if the specified unit is on the given quest.
SpellCanTargetUnit("unit")   - Returns true if the spell awaiting target selection can be cast on the specified unit.
SpellTargetUnit("unit")   - Casts the spell awaiting target selection on the specified unit.
StartDuelUnit("unit")   - Challenge a unit to a duel.
TargetUnit("unit")   - Selects the specified unit as the current target.
UnitAffectingCombat("unit")   - Determine if the unit is in combat or has aggro. (returns nil if "false" and 1 if "true")
UnitArmor("unit")   - Returns the armor statistics relevant to the specified unit.
UnitAttackBothHands("unit")   - Returns information about the unit's melee attacks.
UnitAttackPower("unit")   - Returns the unit's melee attack power and modifiers.
UnitAttackSpeed("unit")   - Returns the unit's melee attack speed for each hand.
UnitBuff("unit", index[, showCastable])   - Retrieves info about a buff of a certain unit.
UnitCanAssist("unit", "otherUnit")   - Returns true if the first unit can assist the second, false otherwise.
UnitCanAttack("unit", "otherUnit")   - Returns true if the first unit can attack the second, false otherwise.
UnitCanCooperate("unit", "otherUnit")   - Returns true if the first unit can cooperate with the second, false otherwise.
UnitCharacterPoints("unit")   - Returns the number of unspent talent points for the specified unit -- usually 0.
UnitClass("unit")   - Returns the class name of the specified unit (e.g., "Warrior" or "Shaman").
UnitClassification("unit")   - Returns the classification of the specified unit (e.g., "elite" or "worldboss").
UnitCreatureFamily("unit")   - Returns the type of creature of the specified unit (e.g., "Crab").
UnitCreatureType("unit")   - Returns the classification type of creature of the specified unit (e.g., "Beast").
UnitDamage("unit")   - Returns the damage statistics relevant to the specified unit.
UnitDebuff("unit", index[, showDispellable])   - Retrieves info about a debuff of a certain unit.
UnitDefense("unit")   - Returns the base defense skill of the specified unit.
UnitExists("unit")   - Returns true if the specified unit exists, false otherwise.
UnitFactionGroup("unit")   - Returns the faction group id and name of the specified unit. (eg. "Alliance")   - string returned is localization-independent (used in filepath)
UnitHealth("unit")   - Returns the current health, in points, of the specified unit.
UnitHealthMax("unit")   - Returns the maximum health, in points, of the specified unit.
UnitInParty("unit")   - Returns true if the unit is a member of your party.
UnitInRaid("unit")   - Returns 1 if unit is in your raid, nil if not.
UnitIsCharmed("unit")   - Returns true if the specified unit is charmed, false otherwise.
UnitIsCivilian("unit")   - Returns true if the unit is a civilian NPC.
UnitIsConnected("unit")   - Returns 1 if the specified unit is connected or npc, nil if offline or not a valid unit.
UnitIsCorpse("unit")   - Returns true if the specified unit is a corpse, false otherwise.
UnitIsDead("unit")   - Returns true if the specified unit is dead, nil otherwise.
UnitIsDeadOrGhost("unit")   - Returns true if the specified unit is dead or a ghost, nil otherwise.
UnitIsEnemy("unit", "otherUnit")   - Returns true if the specified units are enemies, false otherwise.
UnitIsFriend("unit", "otherUnit")   - Returns true if the specified units are friends (PC of same faction or friendly NPC), false otherwise.
UnitIsGhost("unit")   - Returns true if the specified unit is a ghost, false otherwise.
UnitIsPVP("unit")   - Returns true if the specified unit is flagged for PVP, false otherwise.
UnitIsPVPFreeForAll("unit")   - Returns true if the specified unit is flagged for free-for-all PVP, false otherwise.
UnitIsPartyLeader("unit")   - Returns true if the unit is the leader of its party.
UnitIsPlayer("unit")   - Returns true if the specified unit is a player character, false otherwise.
UnitIsPlusMob("unit")   - Returns true if the specified unit is a mob, more powerful than its nominal level, false otherwise (e.g., "elite" mobs)
UnitIsTapped("unit")   - Returns true if the specified unit is tapped, false otherwise.
UnitIsTappedByPlayer("unit")   - Returns true if the specified unit is tapped by the player himself, otherwise false.
UnitIsTrivial("unit")   - Returns true if the specified unit is trivial (Trivial means the unit is "grey" to the player. false otherwise.
UnitIsUnit("unit", "otherUnit")   - Determine if two units are the same unit.
UnitIsVisible("unit")   - 1 if visible, nil if not
UnitLevel("unit")   - Returns the level of a unit.
UnitMana("unit")   - Returns the current mana (or energy,rage,etc), in points, of the specified unit.
UnitManaMax("unit")   - Returns the maximum mana (or energy,rage,etc), in points, of the specified unit.
UnitName("unit")   - Returns the name (and realm name) of a unit.
UnitOnTaxi("unit")   - Returns 1 if unit is on a taxi.
UnitPlayerControlled("unit")   - Returns true if the specified unit is controlled by a player, false otherwise.
UnitPlayerOrPetInParty("unit")   - Returns 1 if the specified unit/pet is a member of the player's party, nil otherwise (returns 1 for "player" and "pet")   - Added in 1.12
UnitPlayerOrPetInRaid("unit")   - Returns 1 if the specified unit/pet is a member of the player's raid, nil otherwise (returns 1 for "player" and "pet")   - Added in 1.12
UnitPVPName("unit")   - Returns unit's name with PvP rank prefix (e.g., "Corporal Allianceguy").
UnitPVPRank("unit")   - Get PvP rank information for requested unit.
UnitPowerType("unit")   - Returns a number corresponding to the power type (e.g., mana, rage or energy) of the specified unit.
UnitRace("unit")   - Returns the race name of the specified unit (e.g., "Human" or "Troll").
UnitRangedAttack("unit")   - Returns the ranged attack number of the unit.
UnitRangedAttackPower("unit")   - Returns the ranged attack power of the unit.
UnitRangedDamage("unit")   - Returns the ranged attack speed and damage of the unit.
UnitReaction("unit", "otherUnit")   - Returns a number corresponding to the reaction (aggressive, neutral or friendly) of the first unit towards the second unit.
UnitResistance("unit", "resistanceIndex")   - Returns the resistance statistics relevant to the specified unit and resistance type.
UnitSex("unit")   - Returns a code indicating the gender of the specified unit, if known. (1=unknown, 2=male, 3=female) ← changed in 1.11!
UnitStat("unit", statIndex)   - Returns the statistics relevant to the specified unit and basic attribute (e.g., strength or intellect).
UnitXP("unit")   - Returns the number of experience points the specified unit has in their current level. (only works on your player)
UnitXPMax("unit")   - Returns the number of experience points the specified unit needs to reach their next level. (only works on your player)
SetPortraitTexture(texture,"unit")   - Paint a Texture object with the specified unit's portrait.
SetPortraitToTexture("texture", icon)   - Paint a Texture object with the given Texture ?
```

## Who Functions
```
GetNumWhoResults()   - Return the number of entries resulting from your most recent /who query.
GetWhoInfo(index)
SendWho("filter")   - Send a who request to the server.
SetWhoToUI(toUIFlag)   - Indicate that who request results should be delivered as WHO_LIST_UPDATE instead of to chat.
SortWho(sortType)   - Sorts an existing /who list; displays the Who List frame if not visible.
```

## Uncategorized Functions
```
PartialPlayTime()
NoPlayTime()
GetBillingTimeRested()
GetMinigameState()
GetMinigameType()
```
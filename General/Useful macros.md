## This guide is from WoWWiki, so all credits go to them!

 

## Spells

Casting spells no longer requires the (Rank x). So you can now have a macro that says: /cast Holy Light, and it’ll cast your highest rank of Holy Light. This macro will always cast the highest rank spell, and you will not be able to cast it on lower-level targets.
Self Cast Any Spell (without losing your target)
```
/script CastSpellByName(‘Holy Light’, 1)
```
 

## Casting buffs

Adapted from the above code, this is designed to cast buffs. If an enemy is selected, you will cast the buff on yourself, if nothing is selected, you will cast the buff on yourself, if you are selected, you will cast the buff on yourself but if your ally is selected they will be buffed.

 

## Example

This macro will cast buffs on you unless an ally is selected (Mark of the Wild):
```
/run if (UnitIsFriend("player", "target") ) then CastSpellByName("Mark of the Wild") else CastSpellByName("Mark of the Wild", 1); end
```
 

## Cast a spell based on target’s class

You’ll need to target the person you want to buff first. Here’s an example for a paladin to use; note that it should all be on one line:
```
/run class = UnitClass("target"); if ( ( class == "Rogue" ) or ( class == "Warrior" ) ) then CastSpellByName("Blessing of Might"); else CastSpellByName("Blessing of Wisdom"); end
```
 

## Cast a spell based on target’s level

You’ll need to target the person you want to buff first. Here’s an example for a priest to use on an English language server. You have to alter the spell name according to the spell you want to cast and change i=6 by the number of ranks you currently have for that spell; note that it should all be on one line:
```
/run Pre="Power Word: Fortitude(Rank " Sp={1,2,14,26,38,50} if (UnitLevel("target") ~= nil and UnitIsFriend("player","target")) then for i=6,1,-1 do if (UnitLevel("target") >= Sp) then CastSpellByName(Pre..i..")") return end end end
```
 

## Cast a healing spell on nearby friends

This will target all your nearby friendly player characters in turn and cast a heal on the first one it comes to with a health level that is below a certain percentage of maximum (in this example 70%). Repeated calls

to the macro will step through all nearby friends needing heals until it targets you. The macro checks the health of up to 40 nearby friendly player characters. If a call to this macro casts no heal then neither nearby friendly player characters nor yourself have a health level below the threshold of 70% of maximum.
```
/run for i=1,40 do TargetNearestFriend();if UnitHealth("target")/UnitHealthMax("target") < 0.7 then if UnitIsPlayer("target") then CastSpellByName("Lesser Healing Wave") end end end; TargetLastEnemy();
```
 

## Announcing spells and targets to your party

Good for healing and crowd control spells. Example with a healing spell (Party member must be targeted first to make the party announcement work):
```
/cast Healing Touch
/party Healing %t in 3.5 seconds
```
 

## Cast a spell on party member based on his location in party

This will target the "first" member of your party, cast a healing spell on him, then return you to your previous target. To use on 2nd member of party change "party1" to "party2".
```
/run TargetUnit("party1")
/cast Flash Heal
/run TargetLastTarget()
```
 

## Cast multiple buffs with smart buff recognition

This script checks whether the target has a buff, if not you cast it, if so you cast a different buff.
```
/run i=1;m=0;while(UnitBuff("target",i)~=nil) do if(strfind(UnitBuff("target",i),"Regeneration")~=nil) then m=1; end;i=i+1;end; c=CastSpellByName; if(m==1) then c("Mark of the Wild(Rank 10)");else c("Thorns(Rank 10)");end;
```
Modify the spell names to change the buff.

 

## Cast even more buffs with smart buff recognition

A lightweight "smart buff" script allowing auto casting of 3 buffs based on your target’s buffs – Buff 3 is cast if you have no target. Requires knowledge of buff names and spell numbers (see Find Buff Name and Search For Spell Number).
```
/run F,C,i,b,t,m,n=strfind,CastSpell,1,"","target" if UnitName(t)~=nil then repeat if F(b,"BNa1") then m=1 elseif F(b,"BNa2") then n=1 end b,i=UnitBuff(t,i),i+1 until b==nil if m==nil then C(BNo1,0) elseif n==nil then C(BNo2,0) end end C(BNo3,0)
```
 

## Find Buff Name

Smart buff recognition requires knowledge of the icon name of the appropriate buff, which may differ from the spell name significantly. The script below lists all buffs currently affecting your target, and these names can be used to modify a smart buffing script for better flexibility.
```
/run i=1; while UnitBuff("target",i)~=nil do DEFAULT_CHAT_FRAME:AddMessage(UnitBuff("target",i)); i=i+1; end
```
Alternatively, this script taken from the Queriable buff effects page also lists debuffs present on your target.
```
/run function m(s) DEFAULT_CHAT_FRAME:AddMessage(s); end for i=1,16 do s=UnitBuff("target", i); if(s) then m("B "..i..": "..s); end s=UnitDebuff("target", i); if(s) then m("D "..i..": "..s); end end
```
 

## Find Spell Number

Sometimes using the CastSpellByName function causes the script to exceed the 255 character limit. In such cases, it may be useful to reference the spell number as found within your spellbook and abilities. This script allows you to poke around looking for the spell number associated with a given spell.

Spells are numbered beginning with all pages found in your general abilities, followed by all pages of your first talent tree then all pages of the second talent tree etc. If you learn new spells and have referenced spells by their number in a script, you may need to revisit this script to ensure you are casting the correct spell and rank.

Guestimate approximately what the spell number might be and modify the number assigned to SpellNumber (26 in the example).

Click the script to view a local display of the spell number, name and rank "Spell 26: Arcane Explosion Rank 6".

Line breaks (carriage returns or ) have been added for legibility only. When copied into WoW, make sure the script is one line only.
```
/run SpellNumber=26; SpellName,SpellRank=GetSpellName(SpellNumber,"spell"); M=format("Spell %d: %s %s",SpellNumber,SpellName,SpellRank); DEFAULT_CHAT_FRAME:AddMessage(M);
```
Once you have the spell number, use CastSpell(spellnumber,0) to cast it. For example if Inner Fire was spell number 17 in your spellbook (as determined using the script above), you could use /run CastSpell(17,0) to cast it.

If you want to ensure that it casts only on yourself, use /run CastSpell(17,0,1).

 

## Search For Spell Number

This modified version of the above script searches for spell numbers that contain a substring defined by the variable f.
```
/run i,s,S=1,"spell",GetSpellName; f="Shadow"; n,r=S(i,"spell") repeat if strfind(n,f)~=nil then m=format("Spell %d: %s %s",i,n,r); DEFAULT_CHAT_FRAME:AddMessage(m); end i=i+1; n,r=S(i,"spell")until n==nil
```
 

## Immediate Cast non-global cooldown Spell

Some spells, such as Amplify Curse and Divine Favor, don’t activate the global cooldown, so it’s possible to immediately follow them with another spell. However, the user interface waits for confirmation of the spellcasting action before allowing you to cast a second spell, which can result in a pause if your connection has some lag. This macro avoids the need for a confirmation by following up with SpellStopCasting, so you can cast a second spell immediately, regardless of lag. Note that if you don’t have the listed spell (Divine Favor, in this example) in your spellbook, running this script will hang your client.
```
/run –CastSpellByName("Divine Favor")
/run local a,i,s,t,j=CastSpellByName,0,"spell","Divine Favor"repeat i=i+1;j=GetSpellName(i,s)until(j==t)j=GetSpellCooldown(i,s)if(j==0)then a(t)SpellStopCasting()end
```
The reason for the first line is so that the icon will show the current cooldown state for the spell correctly.

This macro can be easily modified to allow following it with another spell – append ;CastSpellByName(name_of_spell), and change the starting CastSpellByName to match so you get the cooldown and in-range information for the final spell.
```
/run –CastSpellByName("Curse of Agony")
/run local a,i,s,t,j=CastSpellByName,0,"spell","Amplify Curse"repeat i=i+1;j=GetSpellName(i,s)until(j==t)j=GetSpellCooldown(i,s)if(j==0)then a(t)SpellStopCasting()end;CastSpellByName("Curse of Agony")
```
 

## Equip an item
```
/run PickupContainerItem(bag, slot);
```
bag goes from 0 to 4, and slot from 1 to 20 (depending on bag size).

For more information, go to Item equipping to see how to use items from backpacks, etc., and information on how to prevent accidental vendoring of items due to macros.
 

## Change your boots to Globin Rocket Boots

A really simple script made by myself who changes your boots anyboot you are using to Globin Rocket Boots. Note: Change the MainHandBag and MainBagSlot to where your item are located Note: This macro should be on one line.
```
/run if ( not CursorHasItem() ) then PickupContainerItem(MainHandBag, MainBagSlot);PickupInventoryItem(8); PickupInventoryItem(8); PickupContainerItem(MainHandBag, MainBagSlot); end
```
 

## Quick Self-Bandage
```
/target [Player Name]
/run UseContainerItem(#, #);
/run TargetLastEnemy();
```
Use: Really nice macro for duels or 1v1 pvp. You can stun/fear your enemy, press this and it’ll automatically bandage you without losing your target.

Problem with macro above is losing combo points for rogues. This one will do the same thing without making you lose your combo points
```
/run UseContainerItem(#, #)
/run SpellTargetUnit("player")
```

## Another quick self-bandage from me, Kingoomie. Remember, one line.
```
/run if (not GetContainerItemLink(x,x)) then OpenBag([same bag number as before]); else TargetUnit("player");UseContainerItem(3,15);TargetUnit("playertarget");if (UnitIsPlayer("target")) then ClearTarget() end end
```
Checks for an item in the slot, opens the bag if there isn’t one, uses the item (bandage, in this case) on you, targets your last target, or targets nothing if you either didn’t have a target or were targeting yourself.

 

## Quick Self-Bandage
```
/run TargetUnit("Player")
/run UseAction(ActionID);
/run TargetLastEnemy();
```
For the ActionID, check out the table on the bottom of this chapter. In Basic this does the same as "Quick Self-Bandage by Domandred", but finds the player automatically and uses ActionID instead of ContainerItem.
 

## Use a Bandage
```
/run UseAction(ActionID, 0, 1);
/run if( SpellIsTargeting() ) then SpellTargetUnit("player"); end
```
Bandage must be placed in the action bar at the slot given by ActionID. ActionID is a number from 1 to 120. Slot1-ActionBar1 is ActionID1, Slot12 is ActionID12, Slot1-ActionBar2 is ActionID13 and so on up to Slot12 of ActionBar10. This will bandage your target, or yourself if your current target is not a friendly target.

Here’s a different version courtesy of post by Sarf on the forums. This one will always self-bandage, even if you have a friendly player targeted. It will also re-target your original target. Note that this must all be on one line, its just split up for readability:
```
/run p="player";t="target";if(not UnitCanAttack(t, p))then ot=UnitName(t);TargetUnit(p); else ot=nil;end;UseAction(ActionID);if(SpellIsTargeting())then SpellTargetUnit(p); end if(ot) then TargetByName(ot);end
```
Following is another example of self bandaging that does not use scripting. THIS WILL WORK FOR COSMOS USERS ONLY. Shift-clicking on the bandage (or other item in inventory) while editing your macro will insert its name into your macro. Placing the "target" command after the "use" command maintains your primary target and also maintains your combo points for that target if you’re a Rogue.
```
/use Heavy Linen Bandage
/target player
```

```
/run for b=0,4 do for s=1,GetContainerNumSlots(b) do if (string.find(GetContainerItemLink(b,s) or " ", "Heavy Runecloth Bandage")) then TargetUnit("player"); UseContainerItem(b,s, onSelf); TargetUnit("playertarget") b=4 break end end end
```
Note: As of WoW UI version 1300, when you use the /target command use player not "player" to target yourself. Script command /target does NOT require Cosmos mod, but the /use command does.

You may experience problems with the script above, because it uses non-standard commands. If you place your Heavy bandage in the second ActionBar slot 5 you can use this small macro to use the bandage on your self. This works regardless of whether Cosmos (or any other mod) is installed.
```
/run TargetUnit("player");
/run UseAction(17);
```
You have to use 17, because it is 2nd Actionbar and 5th slot ((2-1)*12+5=17).

## Reference ActionID’s:

Actionbar Slot number <br/>
1: 1 2 3 4 5 6 7 8 9 10 11 12 <br/>
2: 13 14 15 16 17 18 19 20 21 22 23 24 <br/>
3: 25 26 27 28 29 30 31 32 33 34 35 36 <br/>
4: 37 38 39 40 41 42 43 44 45 46 47 48 <br/>
5: 49 50 51 52 53 54 55 56 57 58 59 60 <br/>
6: 61 62 63 64 65 66 67 68 69 70 71 72 <br/>

 

## Use a Trinket/Item
```
/run UseInventoryItem(13)
```
Use: Pops the trinket you have equipped in the first trinket slot. This way if you have several "on use" trinkets you can control any of them with a single button instead of creating multiple buttons for each trinket, as long as the trinket is in the appropriate slot.

For the second trinket slot, substitute (14).

For other "on use" inventory items, substitute the number corresponding to the InventorySlotId.

 

## Sharpen / Apply Poison to Weapon
```
/run UseContainerItem (#,#);
/run PickupInventoryItem (16);
```
Use: Simply press a button and use a Sharpening or Weight stone, or apply a poison. Example: Press a button, sharpen your weapon. Change the 16 or 17 to do it for a secondary weapon. For the #’s on the first line, please refer to "Understanding Location" in section 6.


## Sell all the poor items in your bags
This macro will sell your poor items, when used at a vendor. Rember to put it in one line.
```
/run for bag = 0,4,1 do for slot = 1, GetContainerNumSlots(bag),1 do local name = GetContainerItemLink(bag,slot); if name and string.find(name,"ff9d9d9d") then DEFAULT_CHAT_FRAME:AddMessage("Selling "..name);UseContainerItem(bag,slot) end; end; end
```
 

## Clean bags of poor items

This will delete all poor quality items from your bags. There will be no confirmation dialog – the items will simply vanish. Note that it needs to be on one line, as usual. (/run is a synonym for /script.)

/run ClearCursor()local g,i,j,s,a,b=gsub;for i=0,4 do for j=1,GetContainerNumSlots(i)do s=GetContainerItemLink(i,j)if(s)then a,b,s=GetItemInfo(g(g(s,".*\124H",""),"\124h.*",""))if(s==0)then PickupContainerItem(i,j)DeleteCursorItem()end;end;end;end


## Strip all gear with durability

For those times when you’re not in combat, but about to die anyway (like falling a long distance), this will at least protect your gear (or as much of it as there’s room for in your bags (your backpack will not be used)). Also useful at the right sort of parties. Optimizers can rearrange the slot list to put the most expensive to repair items first. As usual, it needs to be one (really long) line – be careful entering it, as it’s exactly 255 characters long.
```
/run ClearCursor()local k;for i=1,4 do for j=1,GetContainerNumSlots(i)do if(not GetContainerItemLink(i,j))then repeat k,l=next({1,3,5,6,7,8,9,10,16,17,18},k)if(not k)then return;end;PickupInventoryItem(l)until(CursorHasItem())PutItemInBag(i+19)end;end;end
```
 

## Switching Hotbars
```
/run CURRENT_ACTIONBAR_PAGE = X;
/run ChangeActionBarPage();
```
Where X is the Hotbar number

## Example
```
/run CURRENT_ACTIONBAR_PAGE = 1;
/run ChangeActionBarPage(); == Macro Frame Toggling ==
/run if ( not MacroFrame:IsVisible() ) then ShowUIPanel(MacroFrame);else HideUIPanel(MacroFrame); end;
```
 

## Set Video World Environment Variables

Sometimes when you are in a high-traffic area (Ironforge or Orgrimmar in particular), RAM and processors get bogged down. One way to help your computer is to adjust the video settings to improve performance. You can put these macros into hot bars and bind to keys for easy switching, e.g. Shift-\, \, and Ctrl-\ for High, Medium, and Low Res. These don’t change the actual resolution of the screen, only the level of detail. low res is very good for the Auction House / Bank areas. Also, if your UI needs reset (the rendering isn’t working), just switch from one to another.

## HighRes:
```
/z SetFarclip(777)
/z SetWorldDetail(2)
/z SetBaseMip(1)
```

## MediumRes:
```
/z SetFarclip(477)
/z SetWorldDetail(1)
/z SetBaseMip(1)
```

## LowRes:
```
/z SetFarclip(177)
/z SetWorldDetail(0)
/z SetBaseMip(0)
```
 

## Full-screen to windowed mode

I found this handy for working on macros/scripts while having reference material next to me (ie these web pages and others ;). This will switch your game between full-screen, full-colour, and a smaller windowed mode. There are some assumptions, you need to replace the index numbers for your own setting – for me, I run WoW in 1600×1200 32bit full anti-aliasing when full-screen, 1024×768 16bit 1xanti-aliasing when in window. The index numbers can be calculated by going to video options and counting the items on the drop-down.

Note: The bit between "/script" and "/console" must all be on one line (ie there should be a line starting "/script" and a line starting "/console" and that’s it), it’s broken up for readability.

## SwitchMode:
```
/run currentRes = GetCurrentResolution(); if (currentRes == 3) then SetScreenResolution(15); SetCVar("gxWindow", 0); SetMultisampleFormat(16);else SetCVar("gxWindow", 1); SetScreenResolution(3); SetMultisampleFormat(1); end;
```
Replace the "15" in SetScreenResolution with your selected high-res index, the "16" in SetMultisampleFormat with your selected colour depth/anti-aliasing, and the "3" in Set/GetScreenResolution with your preferred windowed res. To finish this one off, drop it into a popup button and go to key bindings, link in "alt-enter". That way, alt-enter will alternate between windowed and full-screen. You can also work in any of the above Farclip etc calls to further alter the settings between windowed and full-screen, depending on how your machine behaves – experiment and see.

Note also, I’m using GetCurrentResolution. I’d rather use GetCVar("gxWindow"), but I got very unreliable results from that – not sure why.
 

## Toggle Name Display

I like to shut off player names when I take screen shots, so here is what I use:
```
/script if ( GetCVar("UnitNamePlayer") == "1" ) then SetCVar("UnitNamePlayer",0) else SetCVar("UnitNamePlayer",1) end
```

## And for shutting off the NPC names I use this:
```
/script if ( GetCVar("UnitNameNPC") == "1" ) then SetCVar("UnitNameNPC",0) else SetCVar("UnitNameNPC",1) end
```
 

## Global Tell Variable

If you have multiple scripts that send tells ("Sheeping Lynk", "Heal Lynk", etc.) it may be useful to have each script reference a global variable that is changed by a single script. Kind of a click once, change em all scenario.

This script sets a global variable PR (Party/Raid) to an appropriate channel based on raid, party or solo membership.

Just click the script to set a global variable that can be referenced by other scripts.

Line breaks (carriage returns or ) have been added for legibility only. When copied into WoW, make sure the script is one line only.
```
/run if (GetNumRaidMembers() > 0) then PR = "Raid"; elseif (GetNumPartyMembers() > 0) then PR = "Party"; else PR = "Say"; end;
```
In your scripts, transpose "Say", "Raid", "Party" for PR.
```
/run SendChatMessage("Lynk is a noob",PR);
```

 

## Select and Auto-attack nearest enemy

This macro is useful for all melee classes. Useful for selecting and auto attacking nearest target, equivalent of pressing Tab, then T by default key bindings with just one key stroke. Hit it multiple times to switch between engaged enemies. It’s useful enough to rebind Tab or Space bar to it.
```
/run AttackTarget();
/run TargetNearestEnemy();
```
 

## Help Tank Character

If you are in a group and fighting a larger group of enemies, and your group tank character is already fighting an enemy, you may not want to attack one which did not have Aggro yet. Select your group tank via key [F] and execute the following macro.
```
/assist %t
/run AttackTarget();
```
If you’re a beginning macro user the above is ok, Better to skip the ‘F’ key and type in the player name in the above. Not sure the AttackTarget(); is safe. But that’s getting into Tactics, so see the Instance Grouping Guide Main Assist page.

A more advanced method of this is to pre-select a player as the "main assist" and have your macro assist that player throughout the duration of the party. The simple method is to replace %t with the name of that player and edit your macro when needed.

Main assist also works for everyday group play, but editing a macro and typing in a player’s name may not be possible in all situations. If you are willing to sacrifice two macros and action bar slots, you can automate things with the following two macros:

## —- Set Main Assist —-
```
/run LeaderPlayerName = UnitName("target") or UnitName("party1") or "";
/run DEFAULT_CHAT_FRAME:AddMessage("######## Set main assist to: " .. LeaderPlayerName);
```

## —- Assist Main Assist Player —-
```
/run AssistByName(LeaderPlayerName or UnitName("party1") or UnitName("player"));
/run DEFAULT_CHAT_FRAME:AddMessage("######## Assisting ".. LeaderPlayerName .. " with target " .. (UnitName("target") or "NO TARGET"));
```
Use the "Set" macro when you have your main assist player selected and want to switch your assist macro to use that player. If no player is selected and you are in a party, the first other party member will be selected. If you are not in a party and not target is selected, you will assist yourself, which is somewhat redundant, but harmless.

To save macro and action bar space, you can combine the two macros in the following script. To set the main assist player, hold down the control key while activating this macro. The version that fits into a 255 character macro is given below and it is somewhat obfuscated:
```
/run p=PAsi or""u=UnitName;t="target"c=IsControlKeyDown()if(c)then p=u(t)or u("party1")or""else AssistByName(p)end;DEFAULT_CHAT_FRAME:AddMessage("######## "..(c and("Set assist: "..p)or("Assisting "..p.." with "..(u(t)or"NO TARGET"))))PAsi=p
```
Here’s the same script with extra spacing and punctuation added for clarity:

## —- Main Assist Utility —-
```
/run p=PAsi or"";u=UnitName;t="target";c=IsControlKeyDown();if(c) then p=u(t) or u("party1") or "" else AssistByName(p)end;DEFAULT_CHAT_FRAME:AddMessage("######## ".. (c and ("Set assist: "..p) or ("Assisting "..p.." with "..(u(t) or "NO TARGET"))));PAsi=p;
```
 

## Assist Main Tank/Main Assist

This script sets your Main Tank or Main Assist for assists and assists the MT/MA all-in-one.

If no MT/MA has been set and you Click the script, you will receive a message stating so "Set MT Noob!".

If you click the script while holding down the Alt key, you will receive a message stating the MT/MA has been set: "MT Set: [Bob]".

If you have set your MT/MA and click the script, you will target your MT/MA’s target.

(This macro should be on one line.)
```
/run if (IsAltKeyDown() and UnitIsFriend("player","target")) then MT=UnitName("target");DEFAULT_CHAT_FRAME:AddMessage(‘MT Set: ['..MT..']‘); elseif (MT ~= nil) then AssistByName(MT);else DEFAULT_CHAT_FRAME:AddMessage(‘Set MT Noob!’); end;
```
 

## Target Memory

The following macro memorizes players and mobs by name. Remembering mobs by name can be a problem if there are several with the exact same name in the area (you will often target the wrong mob). Because of this, this macro should only be used in PvP and when you are fighting a unique boss mob with unique sidekicks.

Hold down control to memorize a target.

To recall a memorized target, use the key without modifiers.

Hold down shift to cast a Polymorph spell on the memorized target.

Alt is ignored, so you can bind this to an alt key combination.

To have multiple memorized targets, edit the Tg1 variable name in the three places where it is mentioned. Note that the short version below uses "ChatFrame1" instead of "DEFAULT_CHAT_FRAME" to save a few characters to allow for longer spell and skill names than Polymorph. The human-readable version is given below the compact/obfuscated version.
```
/run t=Tg1 or""c=IsControlKeyDown()if(c)then t=UnitName("target")or""else TargetByName(t)if(IsShiftKeyDown())then CastSpellByName(‘Polymorph’)end end ChatFrame1:AddMessage("######## "..(c and("Tg1 set to: "..t)or("Targeting: "..t)))Tg1=t
```

## —- Target Memory Utility —-
```
/run t=Tg1 or"" c=IsControlKeyDown() if(c) then t=UnitName("target")or"" else TargetByName(t) if(IsShiftKeyDown()) then CastSpellByName('Polymorph') end end DEFAULT_CHAT_FRAME:AddMessage("######## ".. (c and ("Tg1 set to: "..t) or ("Targeting: "..t))) Tg1=t
```
 

## Kill totems

This can be used to destroy any totem, and is obviously designed for druids. Naturally you can change the last line to /shoot which is especially good for someone with a wand. Whether it will fit in the same macro or not, I’m not certain, but you might also want to add lines to target Dark Iron Dwarf mines as well. I can’t think of anything else like it. The following is from Talashandy, cited by Alex .
```
/target Totem
/cast Moonfire(Rank 1)
```
Here is a bit more programmy way of doing the same thing. Remember to remove the lines breaks.
```
/run u=UnitName;s=strfind;t="target";for i = 1,10,1 do TargetNearestEnemy()if (not UnitCanAttack("player",t))then break;end;if ((s(u(t),"Totem") or s(u(t),"Ward")) and not s(UnitCreatureType(t),"Human")) then CastSpellByName("Shoot");break;end;end;
```
 

## Timer

Simple script to track the time elapsed from a set point in time.

1. Clicking the script while holding the Alt key down will begin the timer and state so.
E.g. "Timer Set: [Instance Start]". <br/>

2. Clicking the script without any additional keys thereafter will yield the time elapsed.
E.g. "Time Elapsed - [Instance Start]: 00h:01m19s".

If you click the script without holding the Alt key first, you will receive an interface error. If you log off for whatever reason,

your timer will be erased. Change "Say" to whatever channel you want "Party", "Raid", "Guild", etc.
```
/run if IsAltKeyDown() then L1="Instance Start"; T1=GetTime(); M=format("Timer Set [%s]",L1); else N=GetTime(); D=N-T1; M=format("Time Elapsed – [%s]: %02dh:%02dm:%02ds",L1, D/3600,mod((D/60),60), mod(D,60)); end; SendChatMessage(M,"SAY");
```

## About script variables

L1 (Label) – Holds the label for the timer. If you have script space, you can copy this script and change L1 to L2, L3 etc. creating multiple timers each with different labels (Core Hound 1, Core Hound 2 etc.)

T1 (Time) – Holds the base time from which time elapsed is computed. For multiple scripts, change T1 to T2, T3 etc.

M (Message) – Temporary variable to hold message formatting.

N (Now) – Temporary variable to hold the current time. Used in computation.

 

## Pet Attack
```
/run PetAttack();
```
A useful extension of this is to have your pet begin assisting your main tank with one button. You could also add a fourth line that casts one of your spells so that you begin fighting too.
```
/target player
/assist
/run PetAttack();
```

## Attack with Dash:
(where Dash is the 4th icon on the pet bar)
```
/run PetAttack(); CastPetAction(4);
```
 

## Pet Passive
```
/run PetPassiveMode();
```
This is really useful in a Scatter Shot macro:
```
/run PetPassiveMode();
/cast Scatter Shot
```
If you use above macro when 5 mobs are attacking your pet at the same time, you pet just comes running to you, so all the mobs will be out of gun/bow range.

If you use the following macro, your pet will start attacking the first mob that attacks him (not the scattershotted one) and he should stay virtually in place.
```
/run PetPassiveMode();
/cast Scatter Shot
/run PetDefensiveMode();
```
 

## Summary of Commands
```
/run PetAggressiveMode();
/run PetDefensiveMode();
/run PetPassiveMode();
/run PetFollow();
/run PetAttack();
/run PetStopAttack();
```
and
```
/run CastPetAction(X);
```
with X being a number on the pet’s action bar (1, 2, 3…)

 

## Local Server time
```
/run hour,min=GetGameTime()
/run DEFAULT_CHAT_FRAME:AddMessage(format("Server time is %s:%s",hour,min));
```
 

## Location
```
/run px,py=GetPlayerMapPosition("player")
/run DEFAULT_CHAT_FRAME:AddMessage(format("[ %s ] %s , %s",GetZoneText(),px,py));
```
Value will be between 0,0 (Top Left corner of current map) and 1,1 (Bottom Right)

A variant that gives a value between 0 and 100, and reduces it to 1 decimal place:
```
/run px,py=GetPlayerMapPosition("player")
/run DEFAULT_CHAT_FRAME:AddMessage(format("%s: %.1f, %.1f",GetZoneText(),px*100,py*100));
```
 

## Change Action Bar Page
```
/run CURRENT_ACTIONBAR_PAGE = X;
/run ChangeActionBarPage();
```
Use: Replace "X" with the action bar page number, and by pressing this, it’ll automatically change. Example: You have two of these, both set on the "=" on page 1 and 2, and have page 1′s set to change to page 2, and vice versa. Whenever you press "=", it’ll toggle between page 1 and 2.

The below macro one does the same thing as the one above, but without the need for two separate macros. It will just switch back and forth between action bar 1 and action bar 4.
```
/run if (CURRENT_ACTIONBAR_PAGE == 1) then CURRENT_ACTIONBAR_PAGE = 4; else CURRENT_ACTIONBAR_PAGE = 1; end; ChangeActionBarPage();
```
 

## Say Quest Objectives
```
/run i = GetNumQuestLeaderBoards(); for j = 1, i, 1 do a1, a2, a3 = GetQuestLogLeaderBoard(j); SendChatMessage(a1, "PARTY"); end;
```
Use: Sends your current quest objectives to your party. This way, you don’t have to constantly type to party members how many of each creature you need to complete a quest.

 

## Turn In Quest Items
```
/script SelectGossipAvailableQuest(1); CompleteQuest(); GetQuestReward();
```
Use: This is usable at almost any quest giver with a blue question mark. It’s especially useful for doing Dark Iron Residue turn ins for Thorium Brotherhood faction. Some of these quest givers offer multiple quests. To have the macro select a quest besides the first one, simply change the number in the parentheses.
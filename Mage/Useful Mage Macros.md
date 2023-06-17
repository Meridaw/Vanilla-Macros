## Offensive Mage Macros

## 1. Anti-Totem
From: Myrafae

This nifty macro targets totems and wands them according to their place on the macro list. It will wand all totems that are in range and than retarget the last target you had before wanding the totems.

Note: This macro will work if you are targeting a shaman only. And will wand the totems in the priortiy of:

Grounding Totem first<br/>
Fire Resistancd Totem second<br/>
Frost Resistance Totem third<br/>
Windfury Totem fourth<br/>
and Earthbind Totem fifth<br/>

```
/script c=CastSpellByName;n=TargetByName;if UnitClass("target")=="Shaman" then n("Earthbind totem") n("Windfury totem") n("Frost Resist") n("Fire Resist") n("Grounding totem") c("Shoot") TargetLastEnemy() else c("Shoot") end;
```


Please understand that this will only work if you are targeting a shaman when you hit this macro, therefore if you are say fighting a priest with a shaman with him who is dropping totems, you need to target the shaman before doing the macro. A different macro that will just check if the target is "horde" and then search for totem is:
```
/script c=CastSpellByName;n=TargetByName;if UnitFactionGroup("target")=="Horde" then n("Earthbind totem") n("Windfury totem") n("Frost Resist") n("Fire Resist") n("Grounding totem") c("Shoot") TargetLastEnemy() else c("Shoot") end;
```


And to stress, one last time, this macro is basically meant as a replacement for your current "Shoot" button 🙂

## 2. Arcane Missiles Fix

If you're tired of the Arcane Missiles bug that causes you to waste mana and channels the spell but doesn't do any damage, use this macro to cast Arcane Missiles from now on. It eliminates the Arcane Missiles bug by preventing overlap, which in turns causes you to be unable to get a "Failed" Arcane Missiles cast.
```
/script cS, W = "Arcane Missiles(Rank 7)", 3
/script --CastSpellByName("Arcane Missiles(Rank 7)")
/script if sA==nil then sT = time(); eT = time() + W; CastSpellByName(cS); sA = true end; if eT <= time() then sA = nil end
```


## 3. Berserking/Spell

This one is for troll mages. It makes sure that you activate Berserking whenever it is up.

This first version cast Berserking when it is up but otherwise cast Frostbolt.
```
/cast Berserking
/cast Frostbolt(Rank 10)
```


This second version cast Berserking if and only if your Health is below 50% (you can change it to whatever percentage you want).
```
/script if UnitHealth('player') / UnitHealthMax('player') < 0.5 then CastSpellByName("Berserking"); end
/cast Frostbolt(Rank 10)
```


The third version checks to see if your target's health is below 20% and if it is than it will just cast Frostbolt instead of activate berserking. Than it checks to see if your HP is below 50% and if it is than you will cast Berserking, else it will cast Frostbolt.
```
/script if UnitHealth('target') / UnitHealthMax('target') < 0.2 then CastSpellByName("Frostbolt(Rank 10)") end;
/script if UnitHealth('player') / UnitHealthMax('player') < 0.5 then CastSpellByName("Berserking"); end
/cast Frostbolt(Rank 10)
```


## 4. Cast to Wand

This macro causes you to normally cast a spell of your choice, but if you run below the mana line, it will automatically Wand for you. Replace "Frostbolt (Rank 10)" with the spell of your choice and "260" with the mana cost of the new spell.
```
/script if (UnitMana("player")>260) then CastSpellByName("Frostbolt (Rank 10)") else CastSpellByName("Shoot") end;
```


## 5. Class SpellChoice

This macro will cast either Frostbolt or Fireball depending on what class you have targeted. You can adjust the classes or the spells to your fitting in this macro.

This example macro will cast Frostbolt on a Rogue or Warrior, and as long as the target isn't a Warlock or Mage, it will cast Fireball.
```
/script x=UnitClass("target");if(x=="Rogue" or x=="Warrior") then CastSpellByName("Frostbolt(Rank 10)");end; else if not(x=="Warlock" or x=="Mage") then CastSpellByName("Fireball(Rank 11)");end;end;
```


## 6. Dismount-Polymorph
From: Lowallyn

This macro causes you to dismount immediately and cast polymorph. Replace the bag# and item# with the slot where your Mount is at.
```
/script UseContainerItem(Bag#, Item#);
/cast Polymorph(Rank 4)
```


## 7. Frostbolt Kiting
From: Geon

This macro causes you to cast Frostbolt (Rank 1) but if you have PoM up, it lets you cast PoM than your highest ranked Frostbolt instead. It is excellent for kiting.
```
/script i=1;m=0;while(UnitBuff("player",i)~=nil) do if(strfind(UnitBuff("player",i),"Spell_Nature_EnchantArmor")~=nil) then m=1; end;i=i+1;end; c=CastSpellByName; if(m==1) then c("Frostbolt");else c("Frostbolt(Rank 1)");end;
```


## 8. Hybrid Assist
From: Graven

Clears your current target and targets the same target as the character you have inputed above.
```
/script ClearTarget();
/assist [Name of Character]
```


## 9. Low-Health Wand

This macro causes you to generally cast Frostbolt (you can change it to whatever you want), but if the target's health is below 5%(you can change this too), it will cause you to cast Wand instead.
```
/script if UnitHealth('target') / UnitHealthMax('target') < 0.05 then CastSpellByName("Shoot") end;
/cast Frostbolt(Rank 10)
```


## 10. Netherwind: Fireball/Pyroblast
From: Gello

This macro usually spams Fireball, but when the Netherwind Focus buff is up, it will cast Pyroblast.
```
/script local f for i=1,24 do f=f or strfind(UnitBuff("player",i) or "","Shadow_Teleport") end if not f then CastSpellByName("Fireball") else CastSpellByName("Pyroblast") end
```


## 11. Scorch to Arcane Missile Clearcasting

This nifty macro would normally cast Scorch (you can replace it with any spell you want) whenever you press it. However, if you have Clearcasting up, it will automatically cast Arcane Missiles instead (or any spell that you want).

Note: Due to server lag, you may have to wait about one second after Clearcasting is up in order for this macro to work. If you are on the new, low population servers and have a fast computer, this should be no problem :].
```
/script local q; local t;for i=0,15,1 do t=GetPlayerBuffTexture(i); if (t and string.find(t, "ManaBurn")) then q=1; break; end; end; if(q ~= nil) then CastSpellByName("Arcane Missiles(Rank 7)") else CastSpellByName("Scorch(Rank 7)"); end;
```


## 12. Shatter: Frozen Attack

This macro usually spams Frostbolt (Rank 1). But when your target is frozen, it cast Frostbolt (Rank 10). You can adjust the spells to whichever you please; some popular variations include Scorch in place of Frostbolt (Rank 1).
```
/script x=UnitDebuff("target");if(x=="Frost Nova" or x=="Frostbite") then CastSpellByName("Frostbolt(Rank 10)");end; else if not(x=="Frost Nova" or x=="Frostbite") then CastSpellByName("Frostbolt(Rank 1)");end;end;
```


## 13. ToEP/ZHC + AP + POM + Pyroblast

Allows you to cast all of these by pressing the same button. You cannot move while doing this however, unless you want to press the button twice. Replace Inventory Item "13" (the Top Trinket Slot) with "14" (the Bottom Trinket Slot) if you have your ToEP/ZHC in the bottom slot.

If you do not have the trinket, simply remove the third and forth line. If you do not have Arcane Power, remove the fifth and sixth line.

Note: You cannot cast both ToEP and ZHC at once because the functionality was removed in 1.10
```
/cast Presence of Mind
/script SpellStopCasting();
/script UseInventoryItem(13);
/script SpellStopCasting();
/cast Arcane Power
/script SpellStopCasting();
/cast Pyroblast
```

If the version above is causing some difficulties, try this alternative version:
```
/script CBN=CastSpellByName;SSC=SpellStopCasting;CBN('Presence of Mind');SSC();UseInventoryItem(13);SSC();UseInventoryItem(13);SSC();CBN('Arcane Power');SSC();CBN('Pyroblast')
```


This alternative version by Jered has the same function but only cast PoM, ToEP/ZHC, and Pyroblast.
```
/cast Presence of Mind
/script SpellStopCasting();
/script s,d,e=GetInventoryItemCooldown("player",13); t=GetTime(); if(s+d<=t and UnitIsEnemy("player","target")) then UseInventoryItem(13); SpellStopCasting(); end; CastSpellByName("Pyroblast");
```


## 14. ToEP/ZHC Safe Cast
From: Graguk's Warlock Macros

When you press this macro, it will activate ToEP/ZHC (depending what you have in the 1st trinket slot) if and only if your target has HP above 30% and is an enemy target. It will than proceed to cast Fireball(Rank 12).
```
/script local a=GetInventorySlotInfo("Trinket1Slot");local b,c=GetInventoryItemCooldown("player",a);if c <= 0 and (UnitHealth("target") > 30 or UnitIsPlayer("target")) then UseInventoryItem(a);SpellStopCasting();end CastSpellByName("Fireball(Rank 12)");
```
 

## Defensive Mage Macros

## 1. Blink: Flip Camera
From: Bardog

This macro causes you to blink, and than flips your camera around to your back. You can change the degree measure to however much you would like to move the camera. This is very useful when blinking past a target, and allowing you to immediately be able to resee the target.

Note: Macros/Mods cannot physically turn your character.

For more information, check out this website: www.wowwiki.com/World_of_Warcraft_API#Camera_Functions
```
/script SpellStopCasting();
/cast Blink
/script FlipCameraYaw(180);
```


## 2. Decurse
From: Pyius

For those unwilling to get decursive, this macro autotargets yourself and removes a curse. It than retargets the last thing you targeted. Insert your name in [your characters name].
```
/target [your characters name]
/cast Remove Lesser Curse
/script TargetLastEnemy();
```


## 3. Frost Nova Ranks

A very simply macro, if you have enough mana it will cast the highest ranked Frost Nova (Rank 4). If you do not have enough mana it will instead cast Frost Nova (Rank 1).
```
/script if ((UnitMana("player"))<65) then CastSpellByName("Frost Nova(Rank 1)");end
/script if ((UnitMana("player"))>=65) then CastSpellByName("Frost Nova");end
```


## 4. Safe Spam Frost Nova
From: They

Attempts to cast Frost nova. If the cooldown of Frost Nova is more than 19 or less than 2, then it will not do anything, all else it will cast Cold Snap.

This macro will prevent you from prematurely using Cold Snap and allow you to mash your Frost Nova in the case of an emergency.

Note: Remember to replace the spell number with the number you have in your spellbook.
```
/script SpellStopCasting(); local start, duration = GetSpellCooldown(57, 0); if ((GetTime() - start) <= 2) or ((GetTime() - start) >= 19) then CastSpell(57,0); else CastSpell(52,0); end
```


An alternative version by Llas merges [Macro 3: Frost Nova Ranks] with this one. It works in this way: If Frost Nova fails, Frost Nova (Rank 1) is tried; then Cold Snap, and if that fails AE is spammed. It also won't call Cold Snap within 5 seconds of the end of cooldown of Frost Nova.

Note: You'll need to substitute the number of your Frost Nova spell for the 110 below. You can adjust the 5 to change the time margin.
```
/cast Frost Nova
/cast Frost Nova(Rank 1)
/script local s,t = GetSpellCooldown(110,"spell"); local l = t- (GetTime()-s); if (l > 5) then CastSpellByName("Cold Snap") ; end
/cast Arcane Explosion
```


## 5. Iceblock/Cold Snap
Note by Rounced

This is one of the more simple macros. It will cast Ice Block normally, but if the cooldown on Ice Block is still up, than it will cast Cold Snap. If you than press it again, it will cast Ice Block once again.

Note: Since 1.10 you can't use macros and Ice Block together. You can use Macros to start Ice Block but you can't use that same Macro to cancel the Ice Block.

This affects the Ice Block/Cold Snap Macro in that it will work but only if you want the Ice Block to last the full 10 seconds every time you cast it.
```
/cast Iceblock
/cast Cold Snap
```


## 6. Iceblock On/Off Macro
From: Cid, Delak

This macro allows you to turn on iceblock and turn off iceblock using two different macros, to eliminate the chance of pressing iceblock too much that it causes it to turn on and off instantly.

To ice block:
```
/script SpellStopCasting(); if (GetSpellCooldown(159,0) == 0) then CastSpell(159,0); end
```


To cancel ice block:
```
/script if (GetTime() - GetSpellCooldown(159,0) < 10) then CastSpell(159,0); end
```


**You'll need to replace 159 with the Id of ice block for you. You can find the Id by counting through your spells from the first page till you get to ice block. The first page means of all spells, so your general tab, not just frost spells.**

If you want to test you have the right spell type this into the chat window:
```
/script DEFAULT_CHAT_FRAME:AddMessage(GetSpellName(X,0));
```


## 7. Ice Barrier/Mana Shield

This macro will cast Ice Barrier when the cooldown is up and Mana Shield when it's not.
```
/cast Ice Barrier(Rank 4)
/cast Mana Shield(Rank 6)
```


## 8. Self-Bandaging

This macro allows you to bandage yourself. You will need to specify the Bag and Item Number in which your bandages lie. After bandaging, you will auto retarget your last target.
```
/script TargetUnit("Player")
/script UseContainerItem(Bag#, Item#);
/script TargetLastEnemy();
```


## 9. Sheep Macro

This macro helps a lot when just starting out in 5 man instances. It informs your party of the target that your are planning to polymorph, so that it is easier for the other members of the party to avoid attacking that target. The macro calls out Sheeping Male/Female Level Target Name. For example, Sheeping Female 60 Onyxia. It also either pops a message in party or raid chat, depending on which you are in.
```
/script if UnitSex("target")==1 then g="female " else g="male " end;s="Sheeping "..g..UnitLevel("target").." %T";c="say";if GetNumRaidMembers()>0 then c="raid" elseif GetNumPartyMembers()>0 then c="party" end;SendChatMessage(s,c)
/cast Polymorph(Rank 4)
```


From Wyzik:
A much more simple one, this one only sends out a call if you are in a party or raid, otherwise it is quiet.
```
/script if UnitSex("target")==1 then g=" Female" else g=" Male" end;s="is sheeping level "..UnitLevel("target")..g.." %T";a=0;if GetPartyMember(1) then a=1;end;if a>0 then SendChatMessage(s,"EMOTE") end;
/cast Polymorph(Rank X)
```


## 10. Stop Casting-Counterspell Macro

This macro stops whatever spell you are currently casting to cast Counterspell. This is extremely useful when you are in the middle of a cast and a priest starts healing. By pressing this, you immediately stop casting and than counterspell the priest.
```
/script SpellStopCasting()
/script CastSpellByName("counterspell")
```


## 11. Toggle: Mage Armor/Ice Armor
From: Foamyla

This macro allows you to toggle between Mage Armor and Ice Armor. If you have Mage Armor on, it will cast Ice Armor, if you have Ice Armor on it will cast Mage Armor.
```
/script local s="Mage" ; for i=1,16 do if strfind(UnitBuff("player",i) or "","MageArmor") then s="Frost" ; break ; end ; end ; CastSpellByName(s.." Armor")
```


## Utility Mage Macros

## 1. All Level Arcane Intellect

This macro allows you to not have to find lower rank Arcane Intellect spells to cast on lower level players. It will cast the highest level Arcane Intellect spell that you have that can be casted on that lower level player.
```
/script r=5;l={1,14,28,42,56};if not UnitIsFriend("player","target")then TargetUnit("player");end;t=UnitLevel("target");for i=r,1,-1 do if (t>=l[ i]-10) then CastSpellByName("Arcane Intellect(Rank "..i..")");break;end;end
```


## 2. Eat/Drink Macro

This macro is for the lazy mages who dont want to figure out when they need to eat or drink. Whenever you fall below 70% in either health or mana, by pressing this macro, you will start to either eat or drink, depending on which is below 70%. This macro, however, requires that you put food in the second backpack slot and water in the first backpack slot.
```
/script if UnitHealth('player') / UnitHealthMax('player') < 0.7 then UseContainerItem(0, 2); end
/script if UnitMana('player') / UnitManaMax('player') < 0.7 then UseContainerItem(0, 1); end
```


## 3. Grey-Trash Selling

This macro sells all the grey items in your bag when you are at a vendor.
```
/script for bag = 0,4,1 do for slot = 1, GetContainerNumSlots(bag), 1 do local name = GetContainerItemLink(bag,slot); if name and string.find(name,"ff9d9d9d") then DEFAULT_CHAT_FRAME:AddMessage("Selling "..name); UseContainerItem(bag,slot) end; end; end
```


## 4. Mana Gems: All-in-One

This macro requires that you put your Mana Ruby in the 14th Slot in your backpack, Mana Citrine in the 15th and Mana Agate in the 16th. This allows you to be able to have one button to use each mana gem whenever the cooldown in between them is up. It saves you the inconvenience of having to open up your backpack or use 3 slots to use the different Mana Gems.

Note: The 14th Slot is the bottom row 2nd spot in your backpack. 15th is the third spot and 16th is the last spot.
```
/script UseContainerItem(0,14);
/script UseContainerItem(0,15);
/script UseContainerItem(0,16);
```


## 5. Open Mail

The first click opens the mail letter, the second click takes up all attachments. Continual pressing will open up all letters and take all attachments.
```
/script GetInboxText(1); TakeInboxItem(1); TakeInboxMoney(1); DeleteInboxItem(1);
```


## 6. Quick Clothes Change
From: Mukiryoku

This macro allows you to take off or wear all of your gear with the click of a button.

To take clothes off:
```
/script local i,j,k=1 myGear={} for j=0,4 do for k=1,GetContainerNumSlots(j) do if not GetContainerItemLink(j,k) then PickupInventoryItem(i) PickupContainerItem(j,k) myGear={j,k} i=i+1 if i>19 then j,k=5,20 end end end end
--------------------------------------------------------------------------------


To put them back on:
```
/script if myGear then local i for i in myGear do PickupContainerItem(myGear[1],myGear[2]) PickupInventoryItem(i) end end
```


## 7. Quick Quest Accept

Allows you to instantly accept a quest. Great for those quest that you need to accept after running through a trail of mobs.
```
/script AcceptQuest()
```


## 8. Self-Buff

Because self cast was banned in 1.10, this macro is very helpful in casting buffs on yourself. It will check to see if you have a target selected, and if you don't it will cast this spell on yourself. If you do, it will cast it on the targeted target.

Note: Replace Arcane Intellect (Rank 5) with whatever spell you want to be self buffed with.
```
/script CastSpellByName("Arcane Intellect(Rank 5)");if((SpellIsTargeting())and(not UnitIsFriend("player","target")))then SpellTargetUnit("player");end;TargetLastEnemy();
```


## 9. Shut Up!
From: Kikyo

This is a nifty macro for those who often face people who randomly open trade and expect food and water. You can replace the message with any message you want. It says this message and than closes the trade window.
```
/say No, I don't have time to make you free stacks of water, unless you want to pay me 5G per stack.
/script CancelTrade()
```


## 10. Waterboy Macro

This macro makes you continually conjure water until you run out of mana (you have to keep pressing it). When you run out of mana, it will use the item in the first slot of your backpack. So, if you want to conjure water and than drink when you are finished, you would put your water in the first slot, and press this macro.
```
/stand
/script if (UnitMana("player")>780) then CastSpellByName("Conjure Water(Rank 7)") else UseContainerItem(0, 1); end;
```


An alternative version cast Evocation whenever it's up and if it isn't, will revert back to conjuring water.
```
/stand
/script if (UnitMana("player")>780) then CastSpellByName("Conjure Water(Rank 7)"); end;
/cast Evocation
/script UseContainerItem(0, 1);
```

 

(\__/) for every nerf the mage class gets, god kills a bunny.<br/>
( ^.^ )<br/>
(")_(") please think of the bunnys.<br/>

 

Made by Lord Mordantes 02.11.2006
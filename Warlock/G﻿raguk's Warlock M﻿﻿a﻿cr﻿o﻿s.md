## 3rd February 2006:

## ZHC and TOEP (Thanks Cominagetcha):
```
/script if GetInventoryItemCooldown("player", 13) == 0 then UseInventoryItem(13); SpellStopCasting(); end
/script if GetInventoryItemCooldown("player", 14) == 0 then UseInventoryItem(14); SpellStopCasting(); end
/cast Shadow Bolt
```
 

## 13th October 2005:

## Updated Siphon Life macro:
```
/script z=0;for i=1,16 do GameTooltipTextLeft1:SetText(nil);GameTooltip:SetUnitDebuff("target",i);if GameTooltipTextLeft1:GetText()=="Siphon Life" then z=1;end;end;if z==1 then TargetNearestEnemy();else CastSpellByName("Siphon Life");end
```

## ToEP and Shadow Bolt macro 
using Astryl's method so it doesn't require 2 presses of the button - it will only activate if your target's health is above 30%, *or* it's a player. It assumes the lower trinket slot - use Trinket0Slot if you have it in the upper slot:
```
/script local a=GetInventorySlotInfo("Trinket1Slot");local b,c=GetInventoryItemCooldown("player",a);if c <= 0 and (UnitHealth("target") > 30 or UnitIsPlayer("target")) then UseInventoryItem(a);SpellStopCasting();end CastSpellByName("Shadow Bolt(rank 9)");
```

## Amplify Curse and Curse of Agony macro
Updated Amplify Curse if it's up (you need to use the "SCAN SPELLBOOK" macro to find the ID in *your* spellbook - change 16 to your ID), then immediately also cast the highest rank of Curse of Agony.
```
/script local e, f, g = GetSpellCooldown(16, SpellBookFrame.bookType); if (f <= 0) then CastSpellByName("Amplify Curse"); SpellStopCasting();end; CastSpellByName("Curse of Agony");
```

## Updated Amplify Curse, else Curse of Exhaustion:
```
/script local e, f, g = GetSpellCooldown(16, SpellBookFrame.bookType); if (f <= 0) then CastSpellByName("Amplify Curse");SpellStopCasting();end; CastSpellByName("Curse of Exhaustion");
```

## Updated Sacrifice, Fel Domination, Summon Voidwalker macro:

First press will Sac a voidwalker (only if it's up), second press activate Fel Domination if it's up and then summon a voidwalker (use the "SCAN SPELLBOOK" macro to find the ID of Fel Domination and Summon Voidwalker in *your* spellbook and replace 16 and 100 respectively with your ID):
```
/script local e,f=GetSpellCooldown(16, SpellBookFrame.bookType);if UnitCreatureFamily("pet") == "Voidwalker" then CastPetAction(5); elseif f<=0 then CastSpellByName("Fel Domination");SpellStopCasting();end; CastSpell(100, SpellBookFrame.bookType);
```

## SCAN SPELLBOOK:

How to find the location of Fel Domination or Amplify Curse etc.

Change "Fel Domination" to "Amplify Curse" if that's what you are looking for. Use this ID in GetSpellCooldown instead of 16 that I use in the examples.
```
/script for id = 1, 180, 1 do local spellName, subSpellName = GetSpellName(id, SpellBookFrame.bookType);if spellName and string.find(spellName, "Fel Domination", 1, true) then ChatFrame1:AddMessage("ID is "..id, 1.0, 1.0, 0.5); end; end;
```
 

Made by Graguk
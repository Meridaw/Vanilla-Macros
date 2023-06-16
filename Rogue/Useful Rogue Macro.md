## Useful Rogue Macro (Updated 03.02.06)

 

## Weapon Switch
```
/script PickupInventoryItem(16);
/script PickupContainerItem(3, 17);
/script PickupInventoryItem(17);
/script PickupContainerItem(3, 18);
```


## Auto Bandaid
```
/script if (UnitCanCooperate("player","target")) then TargetUnit("player"); end UseContainerItem(3, 1); if(SpellIsTargeting()) then TargetUnit("player"); end
/script TargetLastEnemy();
```


## Use Trinket Slot
```
/script UseInventoryItem(13);
```


## Auto Riposte Macro
```
/script if (UnitMana("Player")>=10) and (IsUsableAction(Key#)) then CastSpellByName("Riposte");end;SpellStopCasting();if (UnitMana("Player")>=40) then CastSpellByName("Sinister Strike(Rank 8)"); end
```


## SnD Macro
```
/script GCP=GetComboPoints();if (GCP < style="color: rgb(102, 51, 255);">CastSpellByName("Sinister Strike(Rank 8)") else CastSpellByName("Slice and Dice(Rank 1)"); end
```


## PvE Raid Evis + Feint Macro
```
/script CN=CastSpellByName;GCP=GetComboPoints();if UnitMana("Player")>=20 and IsUsableAction(Key#) then CN("Feint");end;if (GCP>=5) then CN("Eviscerate");end;if UnitMana("Player")>=60 then CN("Backstab");end
```


## Smashable Stealth
```
/script if not(string.find(GetShapeshiftFormInfo(1), "Invis" )) then CastSpellByName("Stealth"); end
```


## Vanish Naked with Itemrack
```
/script CastSpellByName("Vanish(Rank 2)"); EquipSet("Naked");
```


## ZHM Spam Macro
```
/script if (UnitMana("target")>=60) and (GetInventoryItemCooldown("player", 13)==0) then UseInventoryItem(13); end; SpellStopCasting(); CastSpellByName("Backstab(Rank 8)");
```


## CB Eviscerate
```
/script CN=CastSpellByName; CN("Cold Blood"); SpellStopCasting(); if (GetComboPoints()>= 3) then CN("Eviscerate(Rank 8)");end
```


## Todo:

1. Write a smashable shadowmeld+stealth macro

2. Write a smashable SnD + Feint + Rupture macro. Need to detect self buff for this.

 

Posted by VitaminC
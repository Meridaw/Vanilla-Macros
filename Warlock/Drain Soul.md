## Drain Soul, pet passive, delete Soul Shard
```
/cast Drain Soul(Rank 1)
/run PetPassiveMode()local a=GetBagName(4); if a=="Core Felcloth Bag" or a=="Felcloth Bag" or a=="Soul Pouch" or a=="Box of Souls" or a=="Small Soul Pouch" then PickupContainerItem(4,GetContainerNumSlots(4))DeleteCursorItem()end
```
 

## Replace X in the macro with your current version of Drain Soul
```
/cast Drain Soul(Rank X)
/run local a=GetBagName(4); if a=="Core Felcloth Bag" or a=="Felcloth Bag" or a=="Soul Pouch" or a=="Box of Souls" or a=="Small Soul Pouch" then PickupContainerItem(4,GetContainerNumSlots(4)) DeleteCursorItem()end
```
 

## Improved Drain Soul spirit regeneration bonus without competing with pet or having to manually call him off. Keeps him on another target if juggling multiple enemies too.  
```
/run CastSpellByName("Drain Soul(Rank 1)") if UnitIsUnit("playertarget","pettarget") then PetPassiveMode() end
```
 

## Drain Soul, pet passive if pet has player target, delete Soul Shard (edit Soul Pouch)
```
/run CastSpellByName("Drain Soul(Rank 1)") if (UnitIsUnit("playertarget", "pettarget")) then PetPassiveMode()end
/run if GetBagName(4)=="Soul Pouch" then PickupContainerItem(4,GetContainerNumSlots(4))DeleteCursorItem()end
```
 

## Drain Soul rank based on target health and player mana
```
/run if (UnitHealth("target") < 20 || UnitMana("player")) < 1000 then CastSpellByName("Drain Soul(Rank 1)") else CastSpellByName("Drain Soul")end
```
 

## Simple Drain Macro, recalls your pet so DS finishes the target (use pre lvl 20)
```
/cast Drain Soul(Rank 1)
/script CastPetAction(2)
```
## Major Spellstone
create major spellstone, equip and use Spellstone
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Spellstone"))then PickupContainerItem(b,s) EquipCursorItem(17) UseInventoryItem(17)end end end
/cast Create Spellstone (Major)()
```
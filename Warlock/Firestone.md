## Lesser Firestone
makes lesser firestone, equips firestone, uses firestone
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Firestone"))then PickupContainerItem(b,s) EquipCursorItem(17) UseInventoryItem(17)end end end
/cast Create Firestone (Lesser)()
```


## Major Firestone
makes major firestone, equips firestone, uses firestone
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Firestone"))then PickupContainerItem(b,s) EquipCursorItem(17) UseInventoryItem(17)end end end
/cast Create Firestone (Major)()
```
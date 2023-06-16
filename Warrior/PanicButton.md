## PanicButton (edit name of items)
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Quel") or strfind(n,"Draconian"))then PickupContainerItem(b,s)EquipCursorItem(16, 17)end end end
/cast Defensive Stance
/cast Shield Wall
```
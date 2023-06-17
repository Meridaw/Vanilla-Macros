## Swap one hander and shield, cast Flametongue Weapon
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Name One Hander") or strfind(n,"Name Shield"))then PickupContainerItem(b,s)EquipCursorItem(16, 17)end end end
/cast Flametongue Weapon
```
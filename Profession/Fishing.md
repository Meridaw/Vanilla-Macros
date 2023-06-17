## Enchants Aquadynamic Fish Attractor to fishing pole
```
/run for b=0,4 do for s=1,18 do local i=GetContainerItemLink if not(i(b,s)==nil)then if strfind(i(b,s), "Aquadynamic Fish Attractor")then  UseContainerItem(b,s)PickupInventoryItem(16)ReplaceEnchant()end end end end
```
 
## Toggle between the named rod and weapon
While holding shift, toggles between the named rod and weapon. While not holding shift, casts fishing. It doesn't take offhands into account.
```
/run local p,w,z,c,u,l="Fishing Pole","Gnarled Short Staff",string,CastSpellByName,UseItemByName,GetInventoryItemLink("player",16)local s,e=z.find(l,"%[.+%]")l=z.sub(l,s+1,e-1)if IsShiftKeyDown() then if l~=p then u(p)else u(w)end else c("Fishing")end
```
 

## Fishing/Mount/Dismount 
Keybinding this one to a mouse button like middleclick for easy fishing/mounting/dismounting with one hand. put mount in action slot 12.
```
/run local i=GetInventoryItemTexture("player",GetInventorySlotInfo("MainHandSlot")) if i and string.find(i,"INV_Fishingpole")then CastSpellByName("Fishing") else UseAction(12)end
```

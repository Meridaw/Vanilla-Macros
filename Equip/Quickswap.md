## Weapons/Shield quickswap
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (string.find(n,"InsertMainHandName") or string.find(n,"InsertOffHandName"))then PickupContainerItem(b,s)EquipCursorItem(16, 17)break end end end
```
One item got to be mainhand/offhand only, and swap 16 for 17 if both weapons go into main hand slot.

 

## Swap offhand's (Skull of Impending Doom and Misplaced Servo Arm)
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (string.find(n,"Skull of Impending Doom") or string.find(n,"Misplaced Servo Arm"))then PickupContainerItem(b,s)EquipCursorItem(17)break end end end
```
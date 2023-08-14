## Equip item
```
/run for i=0,4 do for j=1,GetContainerNumSlots(i) do if GetContainerItemLink(i,j) then if string.find(GetContainerItemLink(i,j),"Dagger") then PickupContainerItem(i,j) AutoEquipCursorItem() break end end end end
```


## Equip item
```
/run for i=0,4 do for j=1,GetContainerNumSlots(i) do local l=GetContainerItemLink(i,j) if l and string.find(l,"Dagger") then PickupContainerItem(i,j) AutoEquipCursorItem() break end end end
```
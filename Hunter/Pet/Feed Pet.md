## Feed Pet (edit Longjaw Mud Snapper)
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b) do local o=GetContainerItemLink(b,s);if o and string.find(o,"Longjaw Mud Snapper") then CastSpellByName("Feed Pet"); PickupContainerItem(b,s);b=4;break;end;end;end
```


## Drop Wild Hog Shank on pet (replace Wild Hog Shank) 
```
/run local food="Wild Hog Shank"; for bag = 0,4 do for slot = 1,GetContainerNumSlots(bag) do local item = GetContainerItemLink(bag,slot) if item and string.find(item,food) then PickupContainerItem(bag,slot); DropItemOnUnit("pet"); return end end end
```


## Feed pet whatever is in bag 0 slot 1
```
/run CastSpellByName("Feed Pet")PickupContainerItem(0,1)
```
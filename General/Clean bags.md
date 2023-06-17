## Sell all poor items, when used at a vendor
```
/run for bag = 0,4,1 do for slot = 1, GetContainerNumSlots(bag),1 do local name = GetContainerItemLink(bag,slot); if name and string.find(name,"ff9d9d9d") then DEFAULT_CHAT_FRAME:AddMessage("Selling "..name);UseContainerItem(bag,slot) end; end; end
```


## Delete all poor quality items from your bags
```
/run ClearCursor()local g,i,j,s,a,b=gsub;for i=0,4 do for j=1,GetContainerNumSlots(i)do s=GetContainerItemLink(i,j)if(s)then a,b,s=GetItemInfo(g(g(s,".*\124H",""),"\124h.*",""))if(s==0)then PickupContainerItem(i,j)DeleteCursorItem()end;end;end;end
```


## Mass delete item
```
/run for i=0,4 do for j=1,GetContainerNumSlots(i) do if GetContainerItemLink(i,j) then if string.find(GetContainerItemLink(i,j),"Torch") then PickupContainerItem(i,j) DeleteCursorItem() end end end end
```
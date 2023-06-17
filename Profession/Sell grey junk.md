## Sell grey junk
```
/run for bag=0,4,1 do for slot=1,GetContainerNumSlots(bag),1 do local name=GetContainerItemLink(bag,slot) if name and string.find(name,"ff9d9d9d") then DEFAULT_CHAT_FRAME:AddMessage("- Selling "..name) UseContainerItem(bag,slot) end end end
```
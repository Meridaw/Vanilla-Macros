## Enchant any sharpening stone to mainhand, offhand if shift keybind
```
/run for b=0,4 do for s=1,18 do local i=GetContainerItemLink if not(i(b,s)==nil)then if strfind(i(b,s), "Sharpening Stone")then  p=PickupInventoryItem UseContainerItem(b,s)if IsShiftKeyDown()then p(17)else p(16)end ReplaceEnchant()end end end end
```
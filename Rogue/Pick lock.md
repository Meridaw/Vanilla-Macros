## Pick lock Junkbox
```
/run for b = 0,4 do for s=1,GetContainerNumSlots(b) do l=GetContainerItemLink(b,s) if l~=nil then if string.find(l,"Junkbox") then CastSpellByName("Pick Lock") PickupContainerItem(b,s) ClearCursor() end end end end
```
 

## Pick lock Lockbox
```
/run for b = 0,4 do for s=1,GetContainerNumSlots(b,s) do l=GetContainerItemLink(b,s) if l~=nil then if (strfind(l,"Lockbox")) then CastSpellByName("Pick Lock") PickupContainerItem(b,s) ClearCursor() end end end en﻿﻿d
```
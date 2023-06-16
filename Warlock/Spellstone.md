## Create/use Spellstone
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Spellstone"))then UseContainerItem(b,s,1)end end end
/cast Create Spellstone
``` 
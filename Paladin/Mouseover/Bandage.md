## Bandage
```
/run i=(GetMouseFocus().unit) for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Bandage")) and i then UseContainerItem(b,s)SpellTargetUnit(i)end end end
```
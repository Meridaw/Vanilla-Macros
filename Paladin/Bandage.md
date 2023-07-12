## Divine Protection, Self-Bandage
```
/run CastSpellByName("Divine Protection"); for b=0,4 do for s=1,GetContainerNumSlots(b) do local n=GetContainerItemLink(b,s) if n and strfind(n,"Bandage") then UseContainerItem(b,s) TargetUnit("player") end end end
```
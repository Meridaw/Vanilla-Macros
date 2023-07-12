## Target Dummy, Blessing of Protection
uses Target Dummy, aims at dummy and if target is found casts Blessing of Protection
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b) do local n=GetContainerItemLink(b,s) if n and strfind(n,"Dummy")then UseContainerItem(b,s) end end end; TargetByName("Target Dummy");if UnitExists("target")then CastSpellByName("Blessing of Protection")end
```
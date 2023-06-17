## Counterspell unless target Ice Block
```
/run SpellStopCasting() local z=0 for i=1,27 do t=UnitBuff("target",i) if (t and string.find(t,"Frost")) then z=1 break end end if z==0 then CastSpellByName("Counterspell")end
```
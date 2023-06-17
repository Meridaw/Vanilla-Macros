## Inner Fire if missing, else Power Word: Fortitude
```
/run local z=0 for i=1,32 do t=UnitBuff("player",i) if (t and strfind(t,"InnerFire")) then z=1 break end end if z==1 then CastSpellByName("Power Word: Fortitude") else CastSpellByName("Inner Fire")end
```
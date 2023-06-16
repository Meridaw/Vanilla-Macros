## Spammable Prowl
```
/script local i,x=1,0 while UnitBuff("pet",i) do if string.find(UnitBuff("pet",i),"Prowl") then x=1 end i=i+1 end if x==0 then CastSpellByName("Prowl");end
```
## Spammable Feign Death
```
/run local i,x,T=1,0,"player" while UnitBuff(T,i) do if string.find(UnitBuff(T,i), "Feign") then x=1 end i=i+1 end if x==0 then CastSpellByName("Feign Death") else end
```
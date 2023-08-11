## Death Coil + Fear
uses getspellcooldown to track if Death Coil is ready
```
/run local c,s=CastSpellByName,"Death Coil";local i=nil;for j=1,180 do local n=GetSpellName(j,BOOKTYPE_SPELL);if n and strfind(n,s) then i=j;break;end end if i then if GetSpellCooldown(i,BOOKTYPE_SPELL)<1 then c(s)else c("Fear")end end
```


Death Coil + Fear
```
/run if GetSpellCooldown(135,"spell")<1 then CastSpellByName("Death Coil") else CastSpellByName("Fear") end
```
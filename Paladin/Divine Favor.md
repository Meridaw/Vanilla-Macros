## Divine Favor + Holy Shock
```
/run local c,s=CastSpellByName,"Divine Favor";local i=nil;for j=1,180 do local n=GetSpellName(j,BOOKTYPE_SPELL);if n and strfind(n,s) then i=j;break;end end if i then if GetSpellCooldown(i,BOOKTYPE_SPELL)<1 then c(s)else c("Holy Shock")end end
```
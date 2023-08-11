## Inner Focus Time
uses GetTime to track if the 3 min cooldown of inner focus have passed
```
/run if not focusTime then focusTime = 0 end
/run if (GetTime() - focusTime > 180) then CastSpellByName("Inner Focus") focusTime = GetTime() end
/cast Power Word: Shield
```

## Inner Focus + Power Word: Shield
uses getspellcooldown to track if inner focus is ready
```
/run local c,s=CastSpellByName,"Inner Focus";local i=nil;for j=1,180 do local n=GetSpellName(j,BOOKTYPE_SPELL);if n and strfind(n,s) then i=j;break;end end if i then if GetSpellCooldown(i,BOOKTYPE_SPELL)<1 then c(s)else c("Power Word: Shield")end end
```


## Inner Focus + Power Word: Shield
uses Inner Focus if cooldown is ready, else uses Power Word: Shield 
```
/run if GetSpellCooldown(29,'spell')==0 then CastSpellByName("Inner Focus") else CastSpellByName("Power Word: Shield")end
```

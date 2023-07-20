## Inner Focus Time
uses Inner Focus once ever 3 min, then cast Power Word: Shield
```
/run if not focusTime then focusTime = 0 end
/run if (GetTime() - focusTime > 180) then CastSpellByName("Inner Focus") focusTime = GetTime() end
/cast Power Word: Shield
```


## Inner Focus + Power Word: Shield
uses Inner Focus if cooldown is ready, else uses Power Word: Shield 
```
/run if GetSpellCooldown(29,'spell')==0 then CastSpellByName("Inner Focus") else CastSpellByName("Power Word: Shield")end
```

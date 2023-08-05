## Spammable Hurricane
```
/run if not SpellIsTargeting() and not CastingBarFrame.channeling then CastSpellByName("Hurricane")end
```


## Hurrican + Barkskin
```
/run if not focusTime then focusTime = 0 end if (GetTime() - focusTime > 60) then CastSpellByName("Barkskin") focusTime = GetTime() end if not SpellIsTargeting() then CastSpellByName("Hurricane")end
```
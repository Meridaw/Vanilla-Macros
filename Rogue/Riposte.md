## Riposte / Sinister Strike
scans your action bars for Riposte by texture name and uses it if possible. else uses Sinister Strike.
```
/run for i=1,120 do local t=GetActionTexture(i) if t and string.find(t,"Challange") and IsUsableAction(i) and (UnitMana("Player")>=10) then UseAction(i) end if (UnitMana("Player")>=40) then CastSpellByName("Sinister Strike") end end
```


## Riposte & Sinister Strike
Simple macro for PvP Rogues, when you are spamming Sinister strike and dont watch for Reposte, this macro does the work for you. it is necessary that Riposte is binded to the key n.
```
/run local isUsable, IsUsable = IsUsableAction (n);if (isUsable) CastSpellByName("Riposte()") else CastSpellByName("Sinister Strike()");end
```


## Alternative  
Button 61 is on the Blizzard Standart frame the first button on the right bar, Riposte has to be there.
```
/run if (IsUsableAction(61)) then CastSpellByName("Riposte");elseif not (IsUsableAction(61)) then CastSpellByName("Sinister Strike()");end
```


## Riposte / Sinister Strike
```
/cast Riposte
/cast Sinister Strike
```
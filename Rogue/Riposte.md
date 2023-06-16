## Riposte, Sinister Strike
```
/cast Riposte
/cast Sinister Strike
```

## Riposte & Sinister Strike
```
/script local isUsable, IsUsable = IsUsableAction (n);if (isUsable) CastSpellByName("Riposte()") else CastSpellByName("Sinister Strike()");end
```
a really simple macro for PvP Rogues, when you are spamming Sinister strike and dont watch for Reposte, this macro does the work for you.
it will use riposte when ever possible instead of Sinister strike, if its not possible, he keeps using sinister Strike, Simple or? xD
[it is necessary that Riposte is binded to the key n]

## Alternative :
```
/script if (IsUsableAction(61)) then CastSpellByName("Riposte");elseif not (IsUsableAction(61)) then CastSpellByName("Sinister Strike()");end
```
Button 61 is on the Blizzard Standart frame the first button on the right bar, Riposte has to be there
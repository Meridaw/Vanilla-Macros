## Spam stealth, ambush
```
/run local _, _, active = GetShapeshiftFormInfo(1) if not active then CastShapeshiftForm(1)end
/run CastSpellByName("Ambush")
```


## Ambush / Backstab
If stealthed cast Ambush, else cast Backstab
```
/run if (string.find(GetShapeshiftFormInfo(1), "Invis" )) then CastSpellByName("Ambush") else CastSpellByName("Backstab"); end
```
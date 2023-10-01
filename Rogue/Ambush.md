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


## Ambush / Eviscerate / Backstab
```
/run if GetBonusBarOffset() == 1 then CastSpellByName("Ambush") elseif GetComboPoints()>=3 then CastSpellByName("Eviscerate") else CastSpellByName("Backstab")end
```
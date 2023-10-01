## Spam stealth, garrote
```
/run local _, _, active = GetShapeshiftFormInfo(1) if not active then CastShapeshiftForm(1)end
/run CastSpellByName("Garrote")
```


## Garrote / Rupture / Backstab
```
/run if GetBonusBarOffset() == 1 then CastSpellByName("Garrote") elseif GetComboPoints()>=3 then CastSpellByName("Rupture") else CastSpellByName("Backstab")end
```
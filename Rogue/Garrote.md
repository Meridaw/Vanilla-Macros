## Spam stealth, garrote
```
/run local _, _, active = GetShapeshiftFormInfo(1) if not active then CastShapeshiftForm(1)end
/run CastSpellByName("Garrote")
```
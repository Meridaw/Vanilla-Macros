## Spammable bear form/feral charge
```
/run local _, _, active = GetShapeshiftFormInfo(1) if not active or IsControlKeyDown() then CastShapeshiftForm(1) else CastSpellByName("Feral Charge")end
```
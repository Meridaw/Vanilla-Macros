## Stealth + Kidney/Cheap Shot
```
/script if UnitAffectingCombat("player")then CastSpellByName("Kidney Shot")else local _, _, active = GetShapeshiftFormInfo(1) if not active then CastShapeshiftForm(1)end end
/cast Cheap Shot
```
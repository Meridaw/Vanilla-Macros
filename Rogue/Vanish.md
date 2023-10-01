## Vanish / Stealth
```
/run if UnitAffectingCombat("player") then CastSpellByName("Vanish") else CastSpellByName("Stealth") end
```
 

## Vanish / Spammable stealth
```
/run if UnitAffectingCombat("player") then CastSpellByName("Vanish")end local _, _, active = GetShapeshiftFormInfo(1) if not active then CastShapeshiftForm(1)end
```


## Vanish, then Sap
```
/cast Vanish
/script ClearTarget()
/console targetNearestDistance 10
/script TargetNearestEnemy();if UnitIsEnemy("player","target") and not UnitIsDead("target") then CastSpellByName("Sap") end
/console targetNearestDistance 41
```
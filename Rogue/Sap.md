## Sap if target is in range, else clear target
```
/run TargetNearestEnemy()if CheckInteractDistance("target", 3) then CastSpellByName("sap")ClearTarget()else ClearTarget() end
```
 

## Sap
```
/script ClearTarget();
/script TargetNearestEnemy();
/cast Sap
```


## Spam stealth, sap
```
/run local _, _, active = GetShapeshiftFormInfo(1) if not active then CastShapeshiftForm(1)end
/run CastSpellByName("Sap")
```
## Sap if target is in range, else clear target
```
/run TargetNearestEnemy()if CheckInteractDistance("target", 3) then CastSpellByName("sap")ClearTarget()else ClearTarget() end
```
 

## Sap
```
/script ClearTarget();
/script TargetNearestEnemy();
/cast sap
```
 

## Dismount, Stealth, else Sap (put mount in action slot 26)
```
/run a,b,c=GetShapeshiftFormInfo(1);if c then TargetNearestEnemy() CastSpellByName("Sap") else CastSpellByName("Stealth");end
/run i=1 while UnitBuff("player",i) do if string.find(UnitBuff("player",i),"Mount") then UseAction(26)end i=i+1 end
```
 

## Vanish, then Sap
```
/cast Vanish
/script ClearTarget()
/console targetNearestDistance 10
/script TargetNearestEnemy();if UnitIsEnemy("player","target") and not UnitIsDead("target") then CastSpellByName("Sap") end
/console targetNearestDistance 41
```


## Spam stealth, sap
```
/run local _, _, active = GetShapeshiftFormInfo(1) if not active then CastShapeshiftForm(1)end
/run CastSpellByName("Sap")
```
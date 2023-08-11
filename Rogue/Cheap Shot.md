## Cheap Shot, clear target, target last target
```
/cast Cheap Shot
/script ClearTarget();
/script TargetLastTarget();
```


## Spam stealth, cheap shot
```
/run local _, _, active = GetShapeshiftFormInfo(1) if not active then CastShapeshiftForm(1)end
/run CastSpellByName("Cheap Shot")
```
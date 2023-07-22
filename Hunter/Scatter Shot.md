## Scatter Shot
targets the nearest enemy in 15 yards range and fires a scatter shot
```
/console targetNearestDistance 15
/run TargetNearestEnemy() CastSpellByName("Scatter Shot")
/console targetNearestDistance 41
```


## Scatter Shot Rogue
targets nearest enemy then fires a scatter shot and hunter marks the target if rogue
```
/run TargetNearestEnemy(); if (UnitClass("target")=="rogue") then CastSpellByName("Scatter Shot"); CastSpellByName("Hunter's Mark");end
```
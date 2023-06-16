## Targets nearest enemy, Scatter shot and Hunter's Mark if rogue
```
/run TargetNearestEnemy(); if (UnitClass("target")=="rogue") then CastSpellByName("Scatter Shot"); CastSpellByName("Hunter's Mark");end
```
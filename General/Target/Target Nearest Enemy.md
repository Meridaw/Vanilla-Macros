## Target Nearest Enemy
```
/target NearestEnemy();
```


## No Unit Exists
If no target, friendly target, or dead target, then target nearest enemy
```
/script if UnitExists("target") == nil or not UnitIsEnemy("target", "player") or UnitIsDead("target") ~= nil then TargetNearestEnemy() end
```


## Unit Reaction
if no target, no hostile target, then targets nearest enemy
```
/run if GetUnitName("target")==nil or UnitExists("target") and UnitReaction("target","player")>4 then TargetNearestEnemy() end
```
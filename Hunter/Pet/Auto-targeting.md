## Auto-targeting
finds a target and attacks the target if it is not neutral
```
/run for i=1,4 do TargetNearestEnemy(); if UnitIsEnemy("player", "target") then CastPetAction(1); return end end
```
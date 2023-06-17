## Heal anyone in range
This will heal anyone in range who is low on hp. It's set to react on < 40%
```
/script for i=1,40 do TargetNearestFriend(); if UnitHealth("target")/UnitHealthMax("target") < 0.4 then if UnitIsPlayer("target") then CastSpellByName("Lesser Healing Wave(Rank 3)"); end end end; TargetLastEnemy();
```
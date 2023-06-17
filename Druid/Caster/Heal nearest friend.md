## Heal friends in range who is low on hp(Set to react on < 90%)
```
/script for i=1,40 do TargetNearestFriend(); if UnitHealth("target")/UnitHealthMax("target") < 0.9 then if UnitIsPlayer("target") then CastSpellByName("Healing Touch(Rank 3)"); end end end; TargetLastEnemy();
```
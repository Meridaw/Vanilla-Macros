## Auto Target / Sinister Strike
```
/run if UnitExists("target") then CastSpellByName("Sinister Strike") elseif GetUnitName("target")==nil then CastSpellByName("Attack") TargetNearestEnemy() end
```
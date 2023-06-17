## Cure Disease on target if friendly, else Cure Disease oneself
```
/run if UnitIsFriend("player","target") then CastSpellByName("Cure Disease") else CastSpellByName("Cure Disease",1)  end; TargetLastEnemy();
```
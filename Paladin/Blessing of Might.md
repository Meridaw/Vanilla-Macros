## Blessing of Might on target if target is a player, else Blessing of Might on oneself
```
/run if UnitIsFriend ("player", "target") then CastSpellByName("Blessing of Might") else CastSpellByName("Blessing of Might",1)  end; TargetLastEnemy();
```
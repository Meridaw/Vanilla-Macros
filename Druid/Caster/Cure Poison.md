## Cure Poison from target if target is a player, else Cure Poison from oneself
```
/run if UnitIsFriend ("player", "target") then CastSpellByName("Cure Poison") else CastSpellByName("Cure Poison",1)  end; TargetLastEnemy();
```
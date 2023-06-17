## Healing Wave on friendly target, else cast Healing Wave on player
```
/run if UnitIsFriend("player", "target") then CastSpellByName("Healing Wave"); else CastSpellByName("Healing Wave", 1); end
```
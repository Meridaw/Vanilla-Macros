## Blessing of Protection on target if a player, else Blessing of Protection oneself
```
/run if UnitIsFriend ("player", "target") then CastSpellByName("Blessing of Protection") else CastSpellByName("Blessing of Protection",1)  end
```


## Cast Blessing of Protection on the target of your target if this target isn't you
```
/run if not UnitIsUnit("player", "targettarget") then TargetUnit("targettarget") CastSpellByName("Blessing of Protection") TargetLastEnemy() end
```
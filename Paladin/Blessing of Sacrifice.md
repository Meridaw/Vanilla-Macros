## Quicker Blessing of Sacrifice
```
/run TargetNearestFriend()
/cast Blessing of Sacrifice(Rank 1)
```


## Improved Quick Blessing of Sacrifice
```
/run if UnitIsPlayer("target") and not UnitIsUnit("player", "target") then CastSpellByName("Blessing of Sacrifice(Rank 1)") else TargetNearestFriend() end
```
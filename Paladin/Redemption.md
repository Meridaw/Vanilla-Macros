## Redemption, else Holy Light on target / self
```
/run if UnitIsDead("target") then CastSpellByName("Redemption") elseif UnitIsFriend ("player", "target") then CastSpellByName("Holy Light") else CastSpellByName("Holy Light",1)  end
```
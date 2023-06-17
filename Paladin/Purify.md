## Purify target if friendly, else Purify oneself
```
/run if UnitIsFriend ("player", "target") then CastSpellByName("Purify") else CastSpellByName("Purify",1)  end
```
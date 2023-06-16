## Fire Shield on target if friendly, else Fire Shield oneself
```
/run if UnitIsFriend ("player", "target") then CastSpellByName("Fire Shield") else CastSpellByName("Fire Shield",1)  end
```


## Imp Fire Shield
```
/run local c=CastSpellByName if UnitExists("target")then c("Fire Shield")else TargetUnit("player")c("Fire Shield")end ClearTarget()
```
else I'd recommend using TargetLastTarget() instead of ClearTarget() at the end
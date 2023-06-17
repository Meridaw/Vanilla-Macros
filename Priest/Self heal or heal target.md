## Self Flash Heal or Flash Heal player target
```
/run SpellStopCasting()
/run if UnitIsFriend ("player", "target") then CastSpellByName("Flash Heal") else CastSpellByName("Flash Heal",1)  end; TargetLastEnemy();UIErrorsFrame:Clear()
```
 

## Self Heal or Heal player target
```
/run SpellStopCasting()
/run if UnitIsFriend ("player", "target") then CastSpellByName("Heal") else CastSpellByName("Heal",1)  end; TargetLastEnemy();UIErrorsFrame:Clear()
```
 

## Self Lesser Heal or Lesser heal player target
```
/run SpellStopCasting()
/run if UnitIsFriend ("player", "target") then CastSpellByName("Lesser Heal") else CastSpellByName("Lesser Heal",1)  end; TargetLastEnemy();UIErrorsFrame:Clear()
```
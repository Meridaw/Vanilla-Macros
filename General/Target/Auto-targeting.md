## Auto-targeting 
Put these lines ahead of your existing macro for auto-targeting
```
/run if UnitHealth("target")==0 and UnitExists("target") then ClearTarget(); end
/run if GetUnitName("target")==nil then TargetNearestEnemy() end
```


## Spammable Wand Shoot w/ Auto Targeting
```
/run --CastSpellByName("Shoot") end
/run if GetUnitName("target")==nil or UnitExists("target") and UnitReaction("target","player")>4 then TargetNearestEnemy() end
/run if not IsAutoRepeatAction(#) then CastSpellByName("Shoot"); end
```


## Autoshot and melee w/ Auto Targeting
```
/run if GetUnitName("target")==nil then TargetNearestEnemy() end
/run if CheckInteractDistance("target", 3) and (not PlayerFrame.inCombat) then AttackTarget() elseif not IsAutoRepeatAction(#) then CastSpellByName("Auto Shot") end
``` 
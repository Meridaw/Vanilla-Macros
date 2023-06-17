## Flame Shock / Auto Attack
```
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z)end;end;end; CastSpellByName("Flame Shock") UIErrorsFrame:Hide()
```


## Flame Shock, Auto Attack, Target Nearest Enemy
```
/run if not PlayerFrame.inCombat then AttackTarget() end
/cast Flame Shock
/target NearestEnemy();
```
 

## Target enemy, Start attack, cast Flame Shock
```
/run if not PlayerFrame.inCombat then AttackTarget() end if UnitExists("target") == nil or not UnitIsEnemy("target", "player") or UnitIsDead("target") ~= nil then TargetNearestEnemy() end
/cast Flame Shock
```
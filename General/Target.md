## Cast spell on enemy that matches name below EXACTLY. Useful when lvling to tag mobs first.
```
/run TargetByName("REPLACE THIS TO NPC NAME", true) CastSpellByName("REPLACE THIS WITH INSTANT CAST SPELL")
```
 

## Target last target
```
/run TargetLastTarget()
```
 

## Target last enemy
```
/run TargetLastEnemy()
```
 
## Target Nearest Friend
```
/run TargetNearestFriend()
```
 

## Target nearest enemy
```
/target NearestEnemy();
```
 

## If no target, friendly target, or dead target, then target nearest enemy
```
/script if UnitExists("target") == nil or not UnitIsEnemy("target", "player") or UnitIsDead("target") ~= nil then TargetNearestEnemy() end
```
 

## targettarget
```
/run TargetUnit("targettarget") CastSpellByName(spell) TargetLastTarget()
```
 

## Put these lines ahead of your existing macro for auto-targeting
```
/script if UnitHealth("target")==0 and UnitExists("target") then ClearTarget(); end
/run if GetUnitName("target")==nil then TargetNearestEnemy() end
```
 

## Spammable Wand Shoot w/ Auto Targeting
```
/run --CastSpellByName("Shoot") end
/run if GetUnitName("target")==nil or UnitExists("target") and UnitReaction("target","player")>4 then TargetNearestEnemy() end
/script if not IsAutoRepeatAction(#) then CastSpellByName("Shoot"); end
```
 

## Autoshot and melee w/ Auto Targeting
```
/script if GetUnitName("target")==nil then TargetNearestEnemy() end
/run if CheckInteractDistance("target", 3) and (not PlayerFrame.inCombat) then AttackTarget() elseif not IsAutoRepeatAction(3) then CastSpellByName("Auto Shot") end
``` 
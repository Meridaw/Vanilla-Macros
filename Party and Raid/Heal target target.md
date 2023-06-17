## Heal enemy target's target
```
/run if UnitCanAttack("player","target") and not UnitCanAttack("player","targettarget") then TargetUnit("targettarget") CastSpellByName("Heal") TargetLastTarget() end
```
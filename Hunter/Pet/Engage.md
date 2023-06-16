## Engage
```
/run local t='target'if UnitExists(t) and UnitCanAttack('player',t) then PetAttack(t)if CheckInteractDistance('target',3) then CastSpellByName('Attack') else CastSpellByName('Auto Shot') end else TargetNearestEnemy() end
```

Engage allows the Hunter and their pet to attack the target together. This macro also checks the target distance and will use auto melee attack or auto shot attack if the target is close or far enough. I believe the function CheckInteractDistance is looking to see whether the target can be inspected, which happens to be melee range.
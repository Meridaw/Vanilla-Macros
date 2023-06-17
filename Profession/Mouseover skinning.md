## Mouseover Skinning
Use skinning if mouse is over dead target, else target nearest enemy, cast Shadow Bolt
```
/run if UnitIsDead("mouseover") then TargetUnit("mouseover") CastSpellByName("Skinning") else TargetNearestEnemy();CastSpellByName("Shadow Bolt")end
```
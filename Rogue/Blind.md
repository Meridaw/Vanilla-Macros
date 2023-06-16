## Mouseover Blind
```
/run if UnitExists("mouseover")then TargetUnit("mouseover") CastSpellByName("Blind") TargetLastTarget() else CastSpellByName("Blind") end
```
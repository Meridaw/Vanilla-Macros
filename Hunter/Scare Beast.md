## Scare Beast if combat, else Beast Lore
```
/run if UnitAffectingCombat("player") then CastSpellByName("Scare Beast") else CastSpellByName("Beast Lore") end
```


## Mouseover Scare Beast
```
/run if UnitCanAttack("player", "mouseover") and UnitCreatureType("mouseover")=="Beast" then TargetUnit("mouseover") CastSpellByName("Scare Beast") TargetLastTarget() end; PetAttack()
```
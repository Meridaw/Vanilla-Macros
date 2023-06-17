## Cast Detect magic  if enemy, else cast Arcane Intellect
```
/run if UnitCanAttack("player","target") == 1 then CastSpellByName("Detect Magic")else CastSpellByName("Arcane Intellect")end
```
## Turn Undead if combat, else Summon Warhorse
```
/run if UnitAffectingCombat("player") and UnitCreatureType("target")=="Undead" then CastSpellByName("Turn Undead") else CastSpellByName("Summon Warhorse")end
```
## Pet passive, Feign Death if combat, else Wyvern Sting
```
/run PetPassiveMode() if UnitAffectingCombat("player") then CastSpellByName("Feign Death")end
/cast Wyvern Sting
```
## Berserker stance if you are in combat, else Cast Charge
```
/run if UnitAffectingCombat("player") then CastSpellByName("Berserker Stance"); else CastSpellByName("Charge"); end;
```
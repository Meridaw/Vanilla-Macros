## Will change you to zerk or battlestance depending on your combat situation
```
/run if UnitAffectingCombat("player") then CastSpellByName("Berserker Stance"); else CastSpellByName("Battle Stance"); end;
```	
	
	
## Intercept if combat, else Battle Stance
```
/run if UnitAffectingCombat("player") then CastSpellByName("Intercept"); else CastSpellByName("Battle Stance"); end;
```
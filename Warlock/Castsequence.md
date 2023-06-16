## Castsequence Siphon Life, CoA, Corruption, Immolate
```
/run local _gspells = { "Siphon Life", "Curse of Agony", "Corruption", "Immolate"} if GetSpellCooldown(4,"BOOKTYPE_SPELL")==0 then _gi=_gi and _gi > 0 and _gi or 1 CastSpellByName(_gspells[_gi]) _gi = math.mod(1+_gi, 1+table.getn(_gspells))end
```


## Buff Detect Inivisibility, Unending Breath
```
/run local _gspells = { "Detect Invisibility", "Unending Breath"} if GetSpellCooldown(4,"BOOKTYPE_SPELL")==0 then _gi=_gi and _gi > 0 and _gi or 1 CastSpellByName(_gspells[_gi]) _gi = math.mod(1+_gi, 1+table.getn(_gspells))end
```
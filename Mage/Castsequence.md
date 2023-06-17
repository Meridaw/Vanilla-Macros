## Castsequence macro for buffing
```
/run local _gspells = { "Ice Armor", "Dampen Magic", "Arcane Intellect"} if GetSpellCooldown(4,"BOOKTYPE_SPELL")==0 then _gi=_gi and _gi > 0 and _gi or 1 CastSpellByName(_gspells[_gi]) _gi = math.mod(1+_gi, 1+table.getn(_gspells))end
```
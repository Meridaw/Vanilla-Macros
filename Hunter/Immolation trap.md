## Trap/Feign Death
```
/script if UnitAffectingCombat("player") then CastSpellByName("Feign Death") end
/cast Immolation Trap
```


## Immolation trap if alt key, Explosive trap if shift key, else Frost trap
```
/script if IsAltKeyDown() then CastSpellByName("Immolation Trap");elseif IsShiftKeyDown() then CastSpellByName("Explosive Trap"); else CastSpellByName("Frost Trap") end;
```
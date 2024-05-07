## Cast Frostbolt rank 1 if shift key, else max rank
```
/script if IsShiftKeyDown() then CastSpellByName("Frostbolt(Rank 1)") else CastSpellByName("Frostbolt") end
```
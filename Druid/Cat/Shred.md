## Shred/Ferocious Bite (Change 4 to 5 if you want it to build to 5 combo points before Ferocious Bite)
```
/run if GetComboPoints()>=4 then CastSpellByName("Ferocious Bite") else CastSpellByName("Shred") end
```
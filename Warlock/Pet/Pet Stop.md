## Fear + Pet Stop Attack
```
/run if UnitExists("target") then CastSpellByName("Fear") end if UnitExists("pettarget") and UnitIsUnit("target", "pettarget") then PetFollow() PetStopAttack() end
```
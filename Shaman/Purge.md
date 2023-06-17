## Purge if Frost Shock is on cooldown, else Frost Shock
```
/run if GetSpellCooldown(23,'spell')==0 then CastSpellByName("Frost Shock") else CastSpellByName("Purge")end
```
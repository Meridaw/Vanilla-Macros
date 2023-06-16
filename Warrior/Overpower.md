## Overpower
```
/run local texture,name,isActive,isCastable = GetShapeshiftFormInfo(1); if isActive then CastSpellByName("Overpower"); else CastSpellByName("Battle Stance()"); end;
```
 

## Better Overpower
```
/script texture,name,isActive = GetShapeshiftFormInfo(1); if isActive then CastSpellByName("Overpower"); end
/run local start, duration, enabled = GetSpellCooldown(32, BOOKTYPE_SPELL) if duration - ( GetTime() - start) > 1.5 then CastSpellByName("Battle Stance") else cast("Bloodthirst");end
``` 
## Mocking blow/Battle Stance
```
/run local texture,name,isActive,isCastable = GetShapeshiftFormInfo(1); if isActive then CastSpellByName("Mocking Blow"); else CastSpellByName("Battle Stance()"); end;
```
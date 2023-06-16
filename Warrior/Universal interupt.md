## Pummel and Shieldbash in same button
```
/run local texture,name,isActive,isCastable = GetShapeshiftFormInfo(3); if isActive then CastSpellByName("Pummel"); else CastSpellByName("Shield Bash()"); end;
```
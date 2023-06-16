## Whirlwind
```
/run local texture,name,isActive,isCastable = GetShapeshiftFormInfo(3); if isActive then CastSpellByName("Whirlwind"); else CastSpellByName("Berserker Stance()"); end;
```
 

## Casts berserker stance if whirlwind is off cooldown, i have more than 25 rage, and my target is within 8 yards
```
/run local s,d=GetSpellCooldown(46, BOOKTYPE_SPELL) if d~=10 and CheckInteractDistance("target", 3)and (UnitMana("player")>=25)then CastSpellByName("Berserker Stance")end
```
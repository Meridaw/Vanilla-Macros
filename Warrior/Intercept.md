## Intercept
```
/run local texture,name,isActive,isCastable = GetShapeshiftFormInfo(3); if isActive then CastSpellByName("Intercept"); else CastSpellByName("Berserker Stance()"); end;
```
 

## Casts berserker stance if intercept is off cooldown, i have more than 10 rage, and my target further than 8 yards
```
/run local s,d=GetSpellCooldown(40, BOOKTYPE_SPELL) if d~=30 and IsActionInRange(56)==1 and (UnitMana("player")>=10)then CastSpellByName("Berserker Stance")end
```
 

## This macro will use the appropriate ability and change stances depending if youre in or out of combat.
```
/run g=GetShapeshiftFormInfo c=CastSpellByName t,n,bas=g(1) t,n,ber=g(3) if UnitAffectingCombat("player") then if ber then c("Intercept")else c("Berserker Stance")end else if bas then c("Charge")else c("Battle Stance")end end
```
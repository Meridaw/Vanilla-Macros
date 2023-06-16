## Self dispel without losing target
```
/run CastSpellByName('Devour Magic', 1)
```
 

## Casts devour magic on your self if target is hostile
```
/run if UnitExists("pettarget")==1 then if UnitIsFriend("player","pettarget") then CastSpellByName("Devour Magic") else CastSpellByName("Devour Magic", 1)end else TargetLastEnemy()end 
```
 

## Casts Devour Magic on the target, or on mouseover target (without losing current target)
```
/run c=CastSpellByName s="Devour Magic(Rank 4)" if IsShiftKeyDown() then c(s,1) else if UnitExists("mouseover") then TargetUnit("mouseover") c(s) TargetLastTarget() else c(s) end end
```
 

## Cast as normal if friendly target, else self cast
```
/script c=CastSpellByName t=UnitExists f=UnitIsFriend if t("target") and not f("player", "target") then c("Devour Magic", 1) elseif not t("target") then c("Devour Magic", 1) else c("Devour Magic") end;
```
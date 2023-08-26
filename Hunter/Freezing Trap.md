## Trap/Feign Death
```
/script if UnitAffectingCombat("player") then CastSpellByName("Feign Death") end
/cast Freezing Trap
```
 

## Pet on passive/follow/Trap/Feign Death
```
/script PetPassiveMode();
/script PetFollow();
/script if (UnitAffectingCombat("player")) then CastSpellByName("Feign Death") else if not (UnitAffectingCombat("player")) then CastSpellByName("Freezing Trap"); end
```
 

## Feign Death/Trap/Put pet on passive
```
/cast Freezing Trap
/script if UnitAffectingCombat("player") then CastSpellByName("Feign Death") end
/script if UnitExists("pettarget") and CheckInteractDistance("target", 3) and UnitIsUnit("target", "pettarget") then PetPassiveMode(); else end
```
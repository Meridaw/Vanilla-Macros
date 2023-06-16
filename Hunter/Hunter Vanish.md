## NE Hunter Vanish
```
/run PetFollow() PetPassiveMode() ClearTarget() if UnitAffectingCombat("player") then CastSpellByName("Feign Death") else CastSpellByName("Shadowmeld") CastSpellByName("Prowl")end
```
 

## Use any Invisibility potion, Feign Death if combat
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Invisibility Potion"))then UseContainerItem(b,s,1)end end end
/run if UnitAffectingCombat("player") then CastSpellByName("Feign Death") end
```
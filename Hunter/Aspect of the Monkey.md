## Aspect of the Monkey/Raptor Strike
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Ability_Hunter_AspectOfTheMonkey" then x=1 end i=i+1 end if x==0 then CastSpellByName("Aspect of the Monkey") else CastSpellByName("Raptor Strike")end
```
 

## Aspect of the Monkey if melee, else Aspect of the Hawk
```
/run if CheckInteractDistance("target",3) then CastSpellByName("Aspect of the Monkey") else CastSpellByName("Aspect of the Hawk")end
```
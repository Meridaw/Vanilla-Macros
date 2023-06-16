## Aspect of the Hawk if not buffed, else Aimed Shot
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Nature_RavenForm" then x=1 end i=i+1 end if x==0 then CastSpellByName("Aspect of the Hawk") else CastSpellByName("Aimed Shot")end
```
 

## Aspect of the Hawk if not buffed, else Auto Shot (Put Auto Shot into action slot 48)
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Nature_RavenForm" then x=1 end i=i+1 end if x==0 then CastSpellByName("Aspect of the Hawk")else if not IsAutoRepeatAction(48) then UseAction(48)end end
```
 

## Aspect of the Monkey/Raptor Strike
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Ability_Hunter_AspectOfTheMonkey" then x=1 end i=i+1 end if x==0 then CastSpellByName("Aspect of the Monkey") else CastSpellByName("Raptor Strike")end
```
 

## Aspect of the Monkey if melee, else Aspect of the Hawk
```
/run if CheckInteractDistance("target",3) then CastSpellByName("Aspect of the Monkey") else CastSpellByName("Aspect of the Hawk")end
```
 

## Aspect of the Cheetah, else Aspect of the Pack
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Ability_Mount_JungleTiger" then x=1 end i=i+1 end if x==0 then CastSpellByName("Aspect of the Cheetah") else CastSpellByName("Aspect of the Pack") end
```
 

## Aspect of the Cheetah if solo, Pack if party
```
/run if GetNumPartyMembers()==0 and GetNumRaidMembers()==0 then CastSpellByName("Aspect of the Cheetah") else CastSpellByName("Aspect of the Pack") end
```
 

## Aspect of the Hawk/Monkey
```
/run if(UnitBuff("player",1)==nil)then CastSpellByName("Aspect of the Hawk")elseif(string.find(UnitBuff("player",1), "Raven"))then CastSpellByName("Aspect of the Monkey")elseif(UnitBuff("player",1))then CastSpellByName("Aspect of the Hawk");end
```
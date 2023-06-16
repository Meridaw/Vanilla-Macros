If you're targeting a mob and you dont have a mouseover target then the pet will attack your main target and if you do have a mouseover target the pet will attack that target instead so you dont have to switch your own main target and lose DPS
```
/script if UnitCanAttack("player","mouseover") then TargetUnit("mouseover");PetAttack();TargetUnit("playertarget"); else PetAttack(); end
```
 
```
/run local a=UnitExists("mouseover")and"mouseover"or"target"if UnitIsFriend("player",a)then a=a.."target"end;if UnitCanAttack("player",a)then if not UnitIsUnit(a,"pettarget")then TargetUnit(a)PetAttack()return end end;PetFollow()
```
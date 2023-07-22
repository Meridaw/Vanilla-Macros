## Hunter's Mark
uses the hunter's mark on the target if it is not active
```
/run local i,x=1,0 while UnitDebuff("target",i) do if UnitDebuff("target",i)=="Interface\\Icons\\Ability_Hunter_SniperShot" then x=1 end i=i+1 end if x==0 then CastSpellByName("Hunter's Mark")end
```
 

## Hunter's Mark + Pet Attack
uses the hunter's mark and pet attack on the target
```
/run local i,x=1,0 while UnitDebuff("target",i) do if UnitDebuff("target",i)=="Interface\\Icons\\Ability_Hunter_SniperShot" then x=1 end i=i+1 end if x==0 then CastSpellByName("Hunter's Mark") else PetAttack()end
```
 

## Hunter's Mark + Aimed Shot
uses the hunter's mark and aimed shot on the target
```
/run local i,x=1,0 while UnitDebuff("target",i) do if UnitDebuff("target",i)=="Interface\\Icons\\Ability_Hunter_SniperShot" then x=1 end i=i+1 end if x==0 then CastSpellByName("Hunter's Mark") else CastSpellByName("Aimed Shot")end
```
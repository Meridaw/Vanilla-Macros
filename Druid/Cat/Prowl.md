## Cat Form, Prowl, Ravage
```
/run local x,p,t=CastSpellByName,UnitPowerType('Player'),"Ambush" if p==0 then x("Cat Form") elseif p==3 then for i=1,32 do if UnitBuff("player",i) and strfind(UnitBuff("player",i),t) then p=1 end end if p==3 then x("Prowl") else x("Ravage") end end
```


## Cat Form, else Prowl
```
/run local _, _, active = GetShapeshiftFormInfo(3) if not active then CastShapeshiftForm(3) else CastSpellByName("Prowl")end
```


## Prowl/Ravage
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Ability_Ambush" then x=1 end i=i+1 end if x==0 then CastSpellByName("Prowl") else CastSpellByName("Ravage")end
```
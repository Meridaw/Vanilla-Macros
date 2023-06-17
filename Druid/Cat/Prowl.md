## Cat Form, else Prowl
```
/run local _, _, active = GetShapeshiftFormInfo(3) if not active then CastShapeshiftForm(3) else CastSpellByName("Prowl")end
```


## Prowl/Ravage
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Ability_Ambush" then x=1 end i=i+1 end if x==0 then CastSpellByName("Prowl") else CastSpellByName("Ravage")end
```
## Aspect of the Cheetah, else Aspect of the Pack
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Ability_Mount_JungleTiger" then x=1 end i=i+1 end if x==0 then CastSpellByName("Aspect of the Cheetah") else CastSpellByName("Aspect of the Pack") end
```
 

## Aspect of the Cheetah if solo, Pack if party
```
/run if GetNumPartyMembers()==0 and GetNumRaidMembers()==0 then CastSpellByName("Aspect of the Cheetah") else CastSpellByName("Aspect of the Pack") end
```
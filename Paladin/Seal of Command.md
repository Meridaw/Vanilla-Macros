## Seal of Command
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Ability_Warrior_InnerRage" then x=1 end i=i+1 end if x==0 then CastSpellByName("Seal of Command") else CastSpellByName("Judgement")end
```
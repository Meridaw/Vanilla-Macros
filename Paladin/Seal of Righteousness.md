## Seal of Righteousness + Judgement
```
/run local z=0 for i=1,27 do t=UnitBuff("player",i) if (t and strfind(t,"ThunderBolt")) then z=1 break end end if z==1 then CastSpellByName("Judgement") else CastSpellByName("Seal of Righteousness") end 
```
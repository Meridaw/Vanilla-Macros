## Seal of Righteousness + Judgement
```
/run local z=0 for i=1,27 do t=UnitBuff("player",i) if (t and strfind(t,"ThunderBolt")) then z=1 break end end if z==1 then CastSpellByName("Judgement") else CastSpellByName("Seal of Righteousness") end 
```


## Seal of Righteousness
```
/run local z=0 for i=1,27 do t=UnitBuff("player",i) if (t and strfind(t,"ThunderBolt")) then z=1 break end end if z==0 then CastSpellByName("Seal of Righteousness") end
```


## Spammable Righteousness
Seal of Righteousness that cannot be reapplied while buff is up
```
/run i=0;s=0;while(1) do b=GetPlayerBuff(i,"HELPFUL") if b==-1 then break;end t=GetPlayerBuffTexture(b); if string.find(t,"ThunderBolt") then s=1;end i=i+1;end if s==0 or IsControlKeyDown() then CastSpellByName("Seal of Righteousness"); end
```
## Seal of Wisdom + Judgement
```
/run c=CastSpellByName j="Judgement" q="y_Righteou" function b(k)for i=1,32 do if strfind(tostring(UnitBuff("player",i)),k)then return 1 end end end if not b(q) then c("Seal of Wisdom")else c(j) end
```


## Spammable Wisdom
Seal of Wisdom that cannot be reapplied while buff is up
```
/run i=0;s=0;while(1) do b=GetPlayerBuff(i,"HELPFUL") if b==-1 then break;end t=GetPlayerBuffTexture(b); if string.find(t,"RighteousnessAura") then s=1;end i=i+1;end if s==0 or IsControlKeyDown() then CastSpellByName("Seal of Wisdom"); end
```
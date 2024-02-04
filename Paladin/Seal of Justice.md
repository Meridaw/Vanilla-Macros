## Seal of Justice + Judgement
```
/run c=CastSpellByName j="Judgement" q="y_SealOfWrath" function b(k)for i=1,32 do if strfind(tostring(UnitBuff("player",i)),k)then return 1 end end end if not b(q) then c("Seal of Justice")else c(j) end
```


## Seal of Justice
Seal of Justice only when you don't have it active. Judgement if seal is active.
```
/run i=0;s=0;while(1) do b=GetPlayerBuff(i,"HELPFUL") if b==-1 then break;end t=GetPlayerBuffTexture(b);if string.find(t,"SealOfWrath") then CastSpellByName("Judgement");s=1;break;end i=i+1;end;if s==0 then CastSpellByName("Seal of Justice");end;
```
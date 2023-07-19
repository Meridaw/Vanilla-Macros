## Seal of Wisdom + Judgement
```
/run c=CastSpellByName j="Judgement" q="y_Righteou" function b(k)for i=1,32 do if strfind(tostring(UnitBuff("player",i)),k)then return 1 end end end if not b(q) then c("Seal of Wisdom")else c(j) end
```
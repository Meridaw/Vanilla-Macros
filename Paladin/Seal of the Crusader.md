## Seal of the Crusader + Judgement
```
/run c=CastSpellByName j="Judgement" q="y_HolySmite" function b(k)for i=1,32 do if strfind(tostring(UnitBuff("player",i)),k)then return 1 end end end if not b(q) then c("Seal of the Crusader")else c(j) end
```


## Seal of the Crusader and Seal of Righteousness
This one checks for both Seal of the Crusader and Seal of Righteousness and only recasts Seal of Righteousness if none of them are active. This helps a lot when tanking.
```
/run c=CastSpellByName j="Judgement" q="y_ThunderB" r="y_HolyS" function b(k)for i=1,32 do if strfind(tostring(UnitBuff("player",i)),k)then return 1 end end end if b(r)or b(q) then c(j)end if not b(q) and not b(r)then c("Seal of Righteousness")end
```
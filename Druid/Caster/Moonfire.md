## Max rank Moonfire, rank 9 Moonfire if Moonfire debuff on target
```
/run c=CastSpellByName function b(k)for i=1,16 do if strfind(tostring(UnitDebuff("target",i)),k)then return 1 end end end if not b("Nature_StarFall")then c("Moonfire")else c("Moonfire(Rank 9)")end
```
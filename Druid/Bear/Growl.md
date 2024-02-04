## Safe Growl
Safe growl, which protects taunt and growl from being overridden if two or more players spam it at the same time.
```
/run t=0 for i=1,40 do local d=UnitDebuff("target",i) if d then if string.find(d,"UnyieldingFaith") or string.find(d,"Reincarnation") or string.find(d,"Taunt") then t=1 break end end end if t==0 then CastSpellByName("Growl") end
```
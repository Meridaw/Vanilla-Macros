## Renew target if the target does not have Renew
```
/run function b(k)for i=1,32 do if strfind(tostring(UnitBuff("target",i)),k)then return 1 end end end if not b("Renew") then CastSpellByName("Renew")end
```


## Renew target if the target does not have Renew, otherwise renew yourself
```
/run c=CastSpellByName function b(k)for i=1,32 do if strfind(tostring(UnitBuff("target",i or "player",i)),k)then return 1 end end end if not b("Renew") and UnitIsFriend ("player", "target") then c("Renew")elseif not b("Renew")then c("Renew",1)end
```
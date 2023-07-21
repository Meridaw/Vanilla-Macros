## Hunter`s Mark and Pet Attack
```
/run c=CastSpellByName function b(k)for i=1,16 do if strfind(tostring(UnitDebuff("target",i)),k)then return 1 end end end if not b("SniperShot")then c("Hunter's Mark")PetAttack() end
```


## Target nearest enemy, Hunter`s Mark and Pet Attack
```
/run for i=1,4 do TargetNearestEnemy() c=CastSpellByName function b(k)for i=1,16 do if strfind(tostring(UnitDebuff("target",i)),k)then return 1 end end end if not b("SniperShot")then c("Hunter's Mark")PetAttack() end end
```
## Target nearest enemy, Hunter`s Mark and Pet Attack
```
/script if GetUnitName("target")==nil then TargetNearestEnemy() end; CastSpellByName("Hunter's Mark); PetAttack()
```


## Petattack, Hunter's Mark, autoshot (Put Auto Shot in action slot 1)
```
/run PetDefensiveMode() PetAttack() if CheckInteractDistance("target",3) and (not PlayerFrame.inCombat) then AttackTarget() elseif not IsAutoRepeatAction(1) then cast("Auto Shot") end if not buffed("Hunter's Mark",'target') then cast("Hunter's Mark")end
```


## This will find a target and send your pet to attack while keeping him in passive mode, second click will bring pet back to you.
```
/script if GetUnitName("target")==nil then TargetNearestEnemy() end
/script CastPetAction(10);
/script if UnitExists("target") then if a==0 then PetAttack(target) a=1 else if UnitExists("pettarget") and UnitIsUnit("target", "pettarget") then PetFollow("YOURNAMEHERE") a=0 else PetAttack(target) end;end; else PetFollow("YOURNAMEHERE") a=0 end;
```
 

## Modfied the above to also cast Hunter's Mark (just once, will not apply it if the mob is already marked)
```
/script if GetUnitName("target")==nil then TargetNearestEnemy() end
/script CastPetAction(10);
/script if UnitExists("target") then if a==0 then PetAttack(target) a=1 else if UnitExists("pettarget") and UnitIsUnit("target", "pettarget") then PetFollow("YOURNAMEHERE") a=0 else PetAttack(target) end;end; else PetFollow("YOURNAMEHERE") a=0 end
/script if not buffed("Hunter's Mark","target") then CastSpellByName("Hunter's Mark") end
```
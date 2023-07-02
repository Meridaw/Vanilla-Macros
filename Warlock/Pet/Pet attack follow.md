## Pet attack/follow (edit YOURNAMEHERE)
```
/script if UnitExists("target") then if a==0 then PetAttack(target) a=1 else if UnitExists("pettarget") and UnitIsUnit("target", "pettarget") then PetFollow("YOURNAMEHERE") a=0 else PetAttack(target) end;end; else PetFollow("YOURNAMEHERE") a=0 end
```


## Pet attack
```
/run if not UnitExists("target") then PetFollow(); return; end if not UnitIsUnit("target", "pettarget") then PetAttack(target); else PetFollow(); end
```
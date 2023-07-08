## Pet Attack
pet attack if not set to passive or currently attacking
```
/run local _,_,_,_,isActive=GetPetActionInfo(10) if not isActive and not GetUnitName("pettarget") then PetAttack() end
```
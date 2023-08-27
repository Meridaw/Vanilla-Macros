## Curse of Agony + Pet Attack
Curse of Agony and pet attack. If not set to passive or currently attacking.
```
/run local _,_,_,_,isActive=GetPetActionInfo(10) if not isActive and not GetUnitName("pettarget") then PetAttack() end
/cast Curse of Agony
```
## Arcane Shot + Pet Attack
Arcane Shot and pet attack. If not set to passive or currently attacking.
```
/run local _,_,_,_,isActive=GetPetActionInfo(10) if not isActive and not GetUnitName("pettarget") then PetAttack() end
/cast Arcane Shot
```


## Arcane Shot/Auto
```
/run if not GetUnitName("target")then TargetNearestEnemy()end
/cast Arcane Shot(rank 1)
/run if CheckInteractDistance("target", 3)and not PlayerFrame.inCombat then AttackTarget()elseif not IsAutoRepeatAction(3)then CastSpellByName("Auto Shot")end
```
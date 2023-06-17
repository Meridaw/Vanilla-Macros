## Start Melee Attack
```
/script if (not PlayerFrame.inCombat) then AttackTarget() end
```
 

## Auto attack
```
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z);end;end;end;
```
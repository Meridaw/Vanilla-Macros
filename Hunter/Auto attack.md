## Spammable Auto Attack Macro w/ Melee and Ranged swapping 
put Auto Shot into action slot 1 for the range attack to work in this macro
```
/run if CheckInteractDistance("target", 3) and (not PlayerFrame.inCombat) then AttackTarget() elseif not IsAutoRepeatAction(1) then CastSpellByName("Auto Shot") end
```


## Start Melee Attack
```
/script if (not PlayerFrame.inCombat) then AttackTarget() end
```
 

## Spammable Auto attack
```
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z);end;end;end;
```
## Auto attack
```
/run for i=1,120 do if IsCurrentAction(i) then return end end CastSpellByName("Attack")
```


## Start Melee Attack
```
/script if (not PlayerFrame.inCombat) then AttackTarget() end
```
 

## Auto attack
```
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z);end;end;end;
```
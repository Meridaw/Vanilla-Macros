## Auto Attack Macro w/ Melee and Ranged swapping 
put Auto Shot into action slot 1 for the range attack to work in this macro
```
/run if CheckInteractDistance("target", 3) and (not PlayerFrame.inCombat) then AttackTarget() elseif not IsAutoRepeatAction(1) then CastSpellByName("Auto Shot") end
```


## Auto attack
uses a loop to check if attack is set to auto-repeat.
```
/run for i=1,120 do if IsCurrentAction(i) then return end end CastSpellByName("Attack")
```


## Start Melee Attack
this one is decent enough but it is known to be unreliable if spammed.
```
/run if (not PlayerFrame.inCombat) then AttackTarget() end
```
 

## Spammable Auto attack
this one is more reliable. but it requires auto attack to be found on the action bar.
```
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z);end;end;end;
```
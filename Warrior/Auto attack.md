## Spammable Auto Attack Macro w/ Melee and Ranged swapping (put Shoot or Auto Shot into action slot 1)
```
/run if CheckInteractDistance("target", 3) and (not PlayerFrame.inCombat) then AttackTarget() elseif not IsAutoRepeatAction(1) then CastSpellByName("Auto Shot OR Shoot") end
```
Replace Auto Shot or Shoot with your classes ranged auto attack

 

## Start Melee Attack
```
/script if (not PlayerFrame.inCombat) then AttackTarget() end
```
 

## Auto attack
```
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z);end;end;end;
```
 

## Melee shoot
```
/script local _,_,i=strfind(GetInventoryItemLink("player",18),"\124Hitem:(%d+)")local _,_,_,_,_,p=GetItemInfo(i)local t={}t.Bows="Bow"t.Guns="Gun"t.Crossbows="Crossbow"t.Thrown="Throw"CastSpellByName((string.gsub(t[p],"^([^T])","Shoot %1")))
```
## Use any Healthstone/Healing Potion
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Healthstone") or strfind(n,"Healing Potion"))then UseContainerItem(b,s,1)end end end
```
 

Put stone and pot in two different slots, then using a third to activate them with the macro, replace `#` with slot id
```
/run stoneId=# potId=# if IsUsableAction(stoneId) and GetActionCooldown(stoneId) == 0 then UseAction(stoneId) else UseAction(potId) end
```
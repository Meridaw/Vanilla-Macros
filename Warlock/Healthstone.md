## Use any Healthstone/Healing Potion
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Healthstone") or strfind(n,"Healing Potion"))then UseContainerItem(b,s,1)end end end
```
 

## Create/use Healthstone
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Healthstone"))then UseContainerItem(b,s,1)end end end
/cast Create Healthstone (Major)()
```
 

## Healthstone, else healing potion. Put stone and pot in two different slots, then activate them using the macro. (replace `#` with slot id)
```
/run stoneId=# potId=# if IsUsableAction(stoneId) and GetActionCooldown(stoneId) == 0 then UseAction(stoneId) else UseAction(potId) end
```
 

## If Healthstone is on cooldown it uses healing pot, else it uses healthstone. Substitute "slotOfHealthstone" with the numerical slot ID in your actionbar. (SuperMacro)
```
/script if (GetActionCooldown(slotOfHealthstone) ~= 0) then use("Healing Potion") else use("Minor Healthstone") end
```
 

## Trade Healthstone
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s) do local n=GetContainerItemLink(b,s) if n and string.find(n,"Healthstone") then PickupContainerItem(b,s); DropItemOnUnit("target"); AcceptTrade(); break; end; end; end;
```
 

## Trade healthstone
```
/run for i=0,4 do for x=1,GetContainerNumSlots(i) do y=GetContainerItemLink(i,x) if y then if GetItemInfo(y)=="Healthstone" then PickupContainerItem(i,x); DropItemOnUnit("target"); return; end end end end
``` 
## Create Major Soulstone, else use any Soulstone
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Soulstone"))then UseContainerItem(b,s,1)end end end
/cast Create Soulstone (Major)()
```
 

## Create Major Soulstone/Healthstone
```
/run s={"Create Soulstone (Major)()","Create Healthstone (Major)()"} if q==nil then q=0 end q=q+1 if q>getn(s) then q=1 end CastSpellByName(s[q])
```
 

## Use Healthstone if combat, else use Soulstone
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Healthstone") and UnitAffectingCombat("player") or strfind(n,"Soulstone"))then UseContainerItem(b,s,1)end end end
```
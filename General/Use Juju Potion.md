## Use any Juju on yourself, or friendly target (add full name if you want a specific Juju)
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Juju"))then UseContainerItem(b,s)SpellTargetUnit("player")end end end
```
  

## Use any Healthstone/Healing Potion
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Healthstone") or strfind(n,"Healing Potion"))then UseContainerItem(b,s,1)end end end
```
 

## Use any Mana Potion
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Mana Potion"))then UseContainerItem(b,s)end end end
```
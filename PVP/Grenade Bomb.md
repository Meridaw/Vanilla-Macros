## Stop casting, then use any Grenade
```
/run SpellStopCasting() for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Grenade"))then UseContainerItem(b,s)end end end
```
 

## Stop casting, then use any Bomb
```
/run SpellStopCasting() for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Bomb"))then UseContainerItem(b,s)end end end
```
 

## Stop casting, then use any Grenade/Bomb/Dynamite
```
/run SpellStopCasting() for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Bomb" or "Dynamite" or "Grenade"))then UseContainerItem(b,s)end end end
```
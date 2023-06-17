## Use any bandage
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Bandage"))then UseContainerItem(b,s)SpellTargetUnit("player")end end end
```


## Search through your bags and use a bandage on yourself
```
/run TargetUnit("player")function u(n)for b=0,4 do for s=1,GetContainerNumSlots(b)do a=GetContainerItemLink(b,s)if a then if string.find(a,n)then UseContainerItem(b,s,1)return end end end end end u("Bandage")TargetLastTarget()
```
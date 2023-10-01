## Gouge, Bandage oneself
```
/run CastSpellByName("Gouge")for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Bandage"))then UseContainerItem(b,s)SpellTargetUnit("player")end end end
```


## Gouge / Backstab 
If target is Gouged cast Backstab, else cast Gouge
```
/run local i,x=1,0 while UnitDebuff("target",i) do if UnitDebuff("target",i)=="Interface\\Icons\\Ability_Gouge" then x=1 end i=i+1 end if x==0 then CastSpellByName("Gouge") else CastSpellByName("Backstab")end
```
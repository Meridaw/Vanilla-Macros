## Macro for conjuring
```
/script local c=function(a) local f,d a="Mana "..a for i=0,4 do for k=1,GetContainerNumSlots(i) do d=GetContainerItemLink(i,k) or "" if strfind(d,a) then f = 1 end end end if not f then CastSpellByName("Conjure "..a) end end c "Ruby" c "Citrine" c "Jade"
```
 

## Cycling through Conjure Mana
```
/run s={"Conjure Mana Ruby","Conjure Mana Jade","Conjure Mana Citrine","Conjure Mana Agate"} if q==nil then q=0 end q=q+1 if q>getn(s) then q=1 end CastSpellByName(s[q])
```
 

## Use Mana Ruby, Mana Citrine, or Mana Jade
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Mana Ruby") or strfind(n,"Mana Citrine") or strfind(n,"Mana Jade"))then UseContainerItem(b,s,1)end end end
```
## Uses any Conjured water/food (press it quick twice, to eat when you drink)
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Conjured"))then UseContainerItem(b,s,1)end end end
```
 
## Food/Drink

## 1. 
Drag your food in an action button and your drink in another.

## 2. 
Use this command in your chat while hovering your mouse over the "food button" and then the "drink button" and make a note of the numbers it prints.
```
/run local a=GetMouseFocus()message(ActionButton_GetPagedID(a))
```

## 3.
This (all one line) will be your actual food/drink macro after you replace 115,116 with the food button id and drink button id you found above. This will drink if you're not already drinking and eat if you're not already eating. 
```
/run local e,d,s,u,a,p,x,z,f,b,_="INV_Misc_Fork&Knife","INV_Drink_07",strfind,UnitBuff,UseAction,"player",115,116;for i=1,32 do f=(s((u(p,i))or"",e))if(f)then x=nil end;b=(s((u(p,i))or"",d))if(b)then z=nil end;end;_=((x)and a(x))or((z)and a(z))
```﻿
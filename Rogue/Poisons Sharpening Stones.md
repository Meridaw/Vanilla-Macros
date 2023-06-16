## This will apply Instant poison VI on your mainhand if you press on no modifier, and on your offhand if shift is pressed
```
/run for i=0,4 do for j=1,18 do local h=GetContainerItemLink if not(h(i,j)==nil)then if strfind(h(i,j), "Instant Poison VI")then p=PickupInventoryItem UseContainerItem(i,j)if IsShiftKeyDown()then p(17)else p(16)end ReplaceEnchant()end end end end
```
 

## Instant Poison VI to mainhand
```
/run for bag = 0,4,1 do for slot = 1,16,1 do local name = GetContainerItemLink(bag,slot); if name and string.find(name,"Instant Poison VI") then UseContainerItem(bag,slot); PickupInventoryItem(16); ReplaceEnchant(); ClearCursor(); end; end; end
```
 

## Instant Poison VI to offhand
```
/run for bag = 0,4,1 do for slot = 1,16,1 do local name = GetContainerItemLink(bag,slot); if name and string.find(name,"Instant Poison VI") then UseContainerItem(bag,slot); PickupInventoryItem(17); ReplaceEnchant(); ClearCursor(); end; end; end
```
 

## Deadly Poison V to mainhand
```
/run for bag = 0,4,1 do for slot = 1,16,1 do local name = GetContainerItemLink(bag,slot); if name and string.find(name,"Deadly Poison V") then UseContainerItem(bag,slot); PickupInventoryItem(16); ReplaceEnchant(); ClearCursor(); end; end; end
```
 

## Deadly Poison V to offhand
```
/run for bag = 0,4,1 do for slot = 1,16,1 do local name = GetContainerItemLink(bag,slot); if name and string.find(name,"Deadly Poison V") then UseContainerItem(bag,slot); PickupInventoryItem(17); ReplaceEnchant(); ClearCursor(); end; end; end
```
 

## Crippling Poison II to mainhand
```
/run for bag = 0,4,1 do for slot = 1,16,1 do local name = GetContainerItemLink(bag,slot); if name and string.find(name,"Crippling Poison II") then UseContainerItem(bag,slot); PickupInventoryItem(16); ReplaceEnchant(); ClearCursor(); end; end; end
```
 

## Crippling Poison II to offhand
```
/run for bag = 0,4,1 do for slot = 1,16,1 do local name = GetContainerItemLink(bag,slot); if name and string.find(name,"Crippling Poison II") then UseContainerItem(bag,slot); PickupInventoryItem(17); ReplaceEnchant(); ClearCursor(); end; end; end
```
 

## Mind-numbing Poison III to mainhand
```
/run for bag = 0,4,1 do for slot = 1,16,1 do local name = GetContainerItemLink(bag,slot); if name and string.find(name,"Mind%-numbing Poison III") then UseContainerItem(bag,slot); PickupInventoryItem(16); ReplaceEnchant(); ClearCursor(); end; end; end
```
 

## Mind-numbing Poison III to offhand
```
/run for bag = 0,4,1 do for slot = 1,16,1 do local name = GetContainerItemLink(bag,slot); if name and string.find(name,"Mind%-numbing Poison III") then UseContainerItem(bag,slot); PickupInventoryItem(17); ReplaceEnchant(); ClearCursor(); end; end; end
```
 

## Wound Poison IV to mainhand
```
/run for bag = 0,4,1 do for slot = 1,16,1 do local name = GetContainerItemLink(bag,slot); if name and string.find(name,"Wound Poison IV") then UseContainerItem(bag,slot); PickupInventoryItem(16); ReplaceEnchant(); ClearCursor(); end; end; end
```
 

## Wound Poison IV to offhand
```
/run for bag = 0,4,1 do for slot = 1,16,1 do local name = GetContainerItemLink(bag,slot); if name and string.find(name,"Wound Poison IV") then UseContainerItem(bag,slot); PickupInventoryItem(17); ReplaceEnchant(); ClearCursor(); end; end; end
```
 

## Poisons & sharpening Stones

## Mainhand :
```
/script UseContainerItem(x, y)
/script PickupInventoryItem(16)
```

## Offhand :
```
/script UseContainerItem(x, y)
/script PickupInventoryItem(17)
```
 

## Both weapons (2 click) :
```
/run if not a then UseContainerItem(0,2);PickupInventoryItem(16);ReplaceEnchant();ClearCursor();a=1;else UseContainerItem(0,2);PickupInventoryItem(17);ReplaceEnchant();ClearCursor();a=nil;end;
```
 
x = The bag<br/>
y = The slot of the bag<br/>
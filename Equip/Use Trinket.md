## Use trinkets
```
/run UseInventoryItem(13);
/run UseInventoryItem(14);
```
 

## Use trinket if no cooldown
```
/run if  GetInventoryItemCooldown("player", 13)==0 then UseInventoryItem(13)end 
```


## Stops casting spell and use both trinket slots if no cooldown
``` 
/run if GetInventoryItemCooldown("player", 13) == 0 then UseInventoryItem(13); SpellStopCasting(); end
/run if GetInventoryItemCooldown("player", 14) == 0 then UseInventoryItem(14); SpellStopCasting(); end
```


## Trinket if no cooldown, else Shadow Word: Pain
```
/run local s=GetInventoryItemCooldown("player", 13) if s~=0 then CastSpellByName("Shadow Word: Pain") else UseInventoryItem(13) end
```
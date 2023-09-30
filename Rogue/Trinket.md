## Trinket Button
```
/script UseInventoryItem(13);
/script UseInventoryItem(14);
```
 

## Use trinket if no cooldown
```
/run if GetInventoryItemCooldown("player", 13)==0 then UseInventoryItem(13)end
```
 

## Trinket/Rupture
```
/run if GetInventoryItemCooldown("player", 13)==0 then UseInventoryItem(13)end
/run if GetInventoryItemCooldown("player", 14)==0 then UseInventoryItem(14)end
/cast Rupture
``` 
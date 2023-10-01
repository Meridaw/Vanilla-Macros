## Switch weapons between main-hand and off-hand
```
/script PickupInventoryItem(17); PickupInventoryItem(16);
```
both weapons should be one-handed (i mean one-handed weapon marked with "main-hand" label won't be placed in off-hand slot)

 

## The same function but more safe method
```
/script local a,b=CursorHasItem,PickupInventoryItem;if(not a())then CloseMerchant();b(17);if(a())then b(16);end end 
```


## Ambush and Weapon change
```
/cast Ambush(rank 6)
/script PickupContainerItem (x, y)
/script PickupInventoryItem (16)
/script PickupContainerItem (x, y)
/script PickupInventoryItem (17)
/script AttackTarget();
```

x = The bag<br/>
y = The slot of the bag<br/>

After you used Ambush you can switch weapons back to Swords or maces (Kinda useful for enormous burst attacks)(this is meant for bosses NOT FOR PVP)


## How i use
```
/cast Ambush(rank 2)
/script PickupContainerItem (4, 10)
/script PickupInventoryItem (16)
```
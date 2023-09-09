## Weaponswap
this puts your mainhand in the offhand slot, if there is already a weapon in the offhand slot it will switch them around
```
/run PickupInventoryItem(GetInventorySlotInfo("MainHandSlot"));PickupInventoryItem(GetInventorySlotInfo("SecondaryHandSlot"))
```


## Off Hand to Main Hand
this one swaps the main weapon with the off hand weapon
``` 
/run PickupInventoryItem(17); EquipCursorItem(16);
```
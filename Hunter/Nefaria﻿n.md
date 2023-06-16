## Make sure the very first slot in your backpack is open for this to work, your ranged weapon will be put there.
```
/script PickupInventoryItem(18) if ( CursorHasItem() ) then PickupContainerItem(0, 1); else PickupContainerItem(0, 1); PickupInventoryItem(18);end
```
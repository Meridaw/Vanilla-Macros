## Using Trinkets / Inventory Items

Vanilla doesn’t have support for /use command etc. that exists in retail unless you use an addon for it. To use equipment with right click functionality you need to know the slotID.

This example will use the trinket in your top slot:
```	
/run UseInventoryItem(13)
```

## InventorySlots

To use an item in your bags you must know the inventory slotID there as well. You can’t use the item by name. For that you need an addon. My addon Nirklars Keybindings has this functionality with /use added.

The command for using an item in your first bag slot (for example a bandage) on yourself is the following:
```	
/run UseContainerItem(1, 1, 1)
```

## The syntax for the UseContainerItem function is as follows:

UseContainerItem(bagID, slotNumber, UseOnSelf)

BagID

(4) (3) (2) (1) (0)

SlotNumber 

1 2 3 4 <br/>
5 6 7 8 <br/>
9 10 .... etc 

UseOnSelf can be true, false, 0, 1



Made by Sandsten
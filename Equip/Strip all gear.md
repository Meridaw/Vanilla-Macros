## Strip all gear with durability

For those times when you’re not in combat, but about to die anyway (like falling a long distance), this will at least protect your gear (or as much of it as there’s room for in your bags (your backpack will not be used)). Also useful at the right sort of parties. Optimizers can rearrange the slot list to put the most expensive to repair items first. As usual, it needs to be one (really long) line – be careful entering it, as it’s exactly 255 characters long.
```
/run ClearCursor()local k;for i=1,4 do for j=1,GetContainerNumSlots(i)do if(not GetContainerItemLink(i,j))then repeat k,l=next({1,3,5,6,7,8,9,10,16,17,18},k)if(not k)then return;end;PickupInventoryItem(l)until(CursorHasItem())PutItemInBag(i+19)end;end;end
```
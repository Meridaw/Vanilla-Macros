## In the inventory, the slots are numbered like this:

**1_______10**<br/>
**2_______6**<br/>
**3_______7**<br/>
**15______8**<br/>
**4_______11**<br/>
**5_______12**<br/>
**19______13**<br/>
**9_______14**<br/>
**16 17 18**<br/>


## Get Inventory Item Link
print the name and slot of equipped items
```
/run for i=0,23 do if GetInventoryItemLink("player",i) then DEFAULT_CHAT_FRAME:AddMessage("Slot "..i..": "..GetInventoryItemLink("player",i)) end end
```
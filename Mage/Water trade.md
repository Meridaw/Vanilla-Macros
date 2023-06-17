## Trade Water
This macro will open trade, put in two stacks of water, and accept trade in 1 button(click it few times)
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s) do local n=GetContainerItemLink(b,s) if n and string.find(n,"Conjured Crystal Water") then PickupContainerItem(b,s); DropItemOnUnit("target"); AcceptTrade(); break; end; end; end;
```
## Minimap Resize and Move
resizes the minimap scale to 1.5 and allows you to move it around by clicking and dragging with the mouse
```
/run local x,t=Minimap,true x:SetScale(1.5) x:EnableMouse(t) x:SetMovable(t) x:RegisterForDrag("LeftButton") x:SetScript("OnDragStart",function() x:StartMoving() end) x:SetScript("OnDragStop",function() x:StopMovingOrSizing() end)
```


## Moving Minimap to farm mode (adjust the 0, 0 to the coordiantes you'd like to have it)
```
/run Minimap:SetWidth(500); Minimap:SetHeight(500); Minimap:SetPoint("CENTER", UIParent, "CENTER", 0, 0) 
```


## Default size and position 
```
/run Minimap:SetWidth(140); Minimap:SetHeight(140); Minimap:SetPoint("CENTER", UIParent, "CENTER", 755, 380)
```
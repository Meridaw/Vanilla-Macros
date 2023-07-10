## Get Cursor Position
this calculates and prints the coordinates of the cursor
```
/run local x,y=GetCursorPosition() local s=UIParent:GetEffectiveScale() x,y=floor(x/s),floor(y/s) DEFAULT_CHAT_FRAME:AddMessage(format("Cursor: %d, %d",x,y))
```
## Mouseover a action bar button and use this macro to get the ID
```
/run local a=GetMouseFocus()message(ActionButton_GetPagedID(a))
```


## Identify action slot number abilities are placed in and icon name
This will print all the slot and texture names where abilities are placed
```
/run for i=1,72 do if GetActionTexture(i) then DEFAULT_CHAT_FRAME:AddMessage("Slot "..i..": "..GetActionTexture(i))end end
```


## Here you can see where the actionID slots in your actionbars are:

ActionBar page 1: slots 1 to 12<br/>
ActionBar page 2: slots 13 to 24<br/>
ActionBar page 3 (Right ActionBar): slots 25 to 36<br/>
ActionBar page 4 (Right ActionBar 2): slots 37 to 48<br/>
ActionBar page 5 (Bottom Right ActionBar): slots 49 to 60<br/>
ActionBar page 6 (Bottom Left ActionBar): slots 61 to 72<br/>
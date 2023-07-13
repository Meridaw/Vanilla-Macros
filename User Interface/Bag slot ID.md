## Bags are numbered on the right, (4) (3) (2) (1) (0)
Slots in bags are numbered like this:<br/>
1 2 3 4<br/>
5 6 7 8<br/>
9 10 .... etc<br/>


## Use this macro to find bag slot ID:
```
/run DEFAULT_CHAT_FRAME:AddMessage(GetMouseFocus():GetParent():GetID()..", "..GetMouseFocus():GetID())
```
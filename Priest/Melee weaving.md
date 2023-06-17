## Shoot (Mouse wheel up)
```
/run GGUseAction=GGUseAction or UseAction;UseAction=function(id,a,b)if not IsCurrentAction(id)and not IsAutoRepeatAction(id)then GGUseAction(id,a,b)end end CastSpellByName("Shoot") UIErrorsFrame:Hide()
```


## Attack (Mouse wheel down)
``` 
/run GGUseAction=GGUseAction or UseAction;UseAction=function(id,a,b)if not IsCurrentAction(id)and not IsAutoRepeatAction(id)then GGUseAction(id,a,b)end end if CheckInteractDistance("target", 3) then  CastSpellByName("Attack") end UIErrorsFrame:Hide()
```
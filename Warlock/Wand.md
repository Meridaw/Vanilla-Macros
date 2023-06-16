#Shoot (wand)
```
/run if not CastingBarFrame.casting then CastSpellByName("Shoot")end UIErrorsFrame:Hide()
```


#Spammable Shoot
```
/run GGUseAction=GGUseAction or UseAction;UseAction=function(id,a,b)if not IsCurrentAction(id)and not IsAutoRepeatAction(id)then GGUseAction(id,a,b)end end
/cast Shoot
```
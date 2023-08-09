## Shoot
```
/run for i=1,120 do if IsAutoRepeatAction(i) then return end end CastSpellByName("Shoot")
```


## Shoot (wand)
```
/run if not CastingBarFrame.casting then CastSpellByName("Shoot")end UIErrorsFrame:Hide()
```


## Prevent toggling of wand/autoattack
```
/run GGUseAction=GGUseAction or UseAction;UseAction=function(id,a,b)if not IsCurrentAction(id)and not IsAutoRepeatAction(id)then GGUseAction(id,a,b)end end
/cast Shoot
```
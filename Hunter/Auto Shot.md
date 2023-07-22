## Auto Shot
checks for autoshot on your action bar and activates it if it is not activated
```
/run for i=1,120 do local t=GetActionTexture(i) if t and string.find(t,"Weapon") then if not IsAutoRepeatAction(i) then UseAction(i) end end end
```


## Auto Shot
activates auto shot if auto shot is in action slot 1
```
/run if not IsAutoRepeatAction(1) then CastSpellByName("Auto Shot"); end
```
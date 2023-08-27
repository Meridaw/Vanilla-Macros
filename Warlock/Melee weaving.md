## Shoot (Mouse wheel up)
```
/run for i=1,120 do if IsAutoRepeatAction(i) then return end end CastSpellByName("Shoot")
```


## Attack (Mouse wheel down)
``` 
/run for i=1,120 do if IsCurrentAction(i) then return end end if CheckInteractDistance("target", 3) then CastSpellByName("Attack")end
```
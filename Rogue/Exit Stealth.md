## Leave Stealth
```
/run if GetBonusBarOffset() == 1 then CastSpellByName("Stealth") end
```


## Exit Stealth
```
/run local _, _, active = GetShapeshiftFormInfo(1) if active then CastShapeshiftForm(1)end
```


## Unstealth: 
remove stealth. stealth needs to be in action slot 37.
```
/run if IsCurrentAction(37) then UseAction(37) end;
```
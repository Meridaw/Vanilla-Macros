## Caster Form
```
/run for i = 1, GetNumShapeshiftForms() do local _, _, active = GetShapeshiftFormInfo(i) if active then CastShapeshiftForm(i) return end end
```


## Unshift
```
/run for i=1, GetNumShapeshiftForms() do _, name, active = GetShapeshiftFormInfo(i) if( active ~= nil ) then CastShapeshiftForm(i) break end end
```


## Shift out of any Druid form
```
/run for i=1, GetNumShapeshiftForms() do if ({GetShapeshiftFormInfo(i)})[3] then CastShapeshiftForm(i) end end
```
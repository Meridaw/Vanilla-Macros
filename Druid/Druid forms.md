## Spammable Druid forms
```
/run for i=1,5 do if not ({GetShapeshiftFormInfo(2)})[3] then if ({GetShapeshiftFormInfo(i)})[3] then CastShapeshiftForm(i) end CastShapeshiftForm(2) end end
```

Shapeshift Forms go from left to right: 1 is Bear, 2 is Cat, etc
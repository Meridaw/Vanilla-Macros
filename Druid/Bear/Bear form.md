## Bear Form from any form, 2 clicks.
```
/run local s,_ for i=1,5 do _,_,s=GetShapeshiftFormInfo(i)if s then CastShapeshiftForm(i)break end end if not s then CastShapeshiftForm(1) end
```


## Spammable Bear Form
```
/run for i=1,5 do if not ({GetShapeshiftFormInfo(1)})[3] then if ({GetShapeshiftFormInfo(i)})[3] then CastShapeshiftForm(i) end CastShapeshiftForm(1) end end
```
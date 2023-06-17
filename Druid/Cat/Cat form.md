## Spammable cat form
```
/run local _, _, active = GetShapeshiftFormInfo(3) if not active then CastShapeshiftForm(3)end
```


## Cat Form / Prowl
```
/run local _, _, active = GetShapeshiftFormInfo(3) if not active or IsControlKeyDown() then CastShapeshiftForm(3) else CastSpellByName"Prowl" end
```


## Spammable cat form, Track Humanoids
```
/run local _, _, active = GetShapeshiftFormInfo(3) if not active then CastShapeshiftForm(3)end
/cast Track Humanoids
```
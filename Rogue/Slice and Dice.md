## Slice and Dice / Sinister Strike
```
/run local z=0 for i=1,27 do t=UnitBuff("player",i) if (t and strfind(t,"SliceDice")) then z=1 break end end if z==0 and (GetComboPoints()>=1) then CastSpellByName("Slice and Dice") else CastSpellByName("Sinister Strike")end
```


## Slice and Dice / Backstab
```
/run local z=0 for i=1,27 do t=UnitBuff("player",i) if (t and strfind(t,"SliceDice")) then z=1 break end end if z==0 and (GetComboPoints()>=1) then CastSpellByName("Slice and Dice") else CastSpellByName("Backstab")end
```
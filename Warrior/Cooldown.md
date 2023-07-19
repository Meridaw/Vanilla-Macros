## Recklessness / Shield Wall / Retaliation
```
/run local x=CastSpellByName _,n=GetShapeshiftFormInfo(1)if n=="Battle Stance"then x("Retaliation")elseif n=="Defensive Stance"then x("Shield Wall")else x("Berserker Stance")end _,n=GetShapeshiftFormInfo(3)if n=="Berserker Stance"then x("Recklessness")end
```
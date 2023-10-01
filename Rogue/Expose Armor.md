## Expose Armor without doing DMG
```
/run CastSpellByName("Expose Armor")
/run ClearTarget();
```
you could use that in Duels, when you Gauge an enemy, using this makro to reduce his armor without getting him out of the CC and than go into stealth, BÄM AMBUSH. now thats going to hurt.


## Expose Armor / Gouge
Expose Armor if +1 combo else Gouge
```
/run if GetComboPoints()>=1 then CastSpellByName("Expose Armor") else CastSpellByName("Gouge") end UIErrorsFrame:Hide()
/run ClearTarget() TargetLastTarget()
```
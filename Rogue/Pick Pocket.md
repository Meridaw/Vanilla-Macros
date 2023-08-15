## Pick Pocket / Backstab
uses Backstab if target is found or pick pocket if only mouseover is found. 
```
/run if UnitExists("target") then CastSpellByName("Backstab") elseif UnitExists("mouseover") then SpellTargetUnit("mouseover") TargetUnit("mouseover") CastSpellByName("Pick Pocket")end
```


## Pick Pocket / Ambush 
```
/run if n~= 1 then CastSpellByName("Pick Pocket") n=1 else CastSpellByName("Ambush") n=0 end;
```


## Modifier key
Uses Pick Pocket while Shift is being hold down, else Ambush.
```
/run if (IsShiftKeyDown())then CastSpellByName("Pick Pocket") else CastSpellByName("Ambush") end
```
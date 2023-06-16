## Taunt
```
/run local texture,name,isActive,isCastable = GetShapeshiftFormInfo(2); if isActive then CastSpellByName("Taunt"); else CastSpellByName("Defensive Stance()"); end;
```
 

## Taunt your current target if it does not target you
```
/run if not UnitIsUnit('player', 'targettarget') then CastSpellByName('Taunt'); en﻿d
```
## Taunt
```
/run local texture,name,isActive,isCastable = GetShapeshiftFormInfo(2); if isActive then CastSpellByName("Taunt"); else CastSpellByName("Defensive Stance()"); end;
```
 

## Taunt your current target if it does not target you
```
/run if not UnitIsUnit('player', 'targettarget') then CastSpellByName('Taunt'); en﻿d
```


## Taunt Emote
```
/cast Taunt
/run if not TeM then TeM = GetTime() + 10 end
/run if GetTime() > TeM then DoEmote("taunt") TeM = nil end
```
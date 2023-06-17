## Self cast Cleanse
```
/run C=CastSpellByName; A="Cleanse" if UnitIsFriend("player","target") then C(A) else if not UnitIsFriend("player","target") then C(A, 1) end; end;
```
 

## Cleanse macro
```
/script local p,q="player",nil if UnitCanAssist("target",p) then ClearTarget() q=0 end CastSpellByName("Cleanse()") SpellTargetUnit(p) if q then AssistUnit(p) en﻿d
```
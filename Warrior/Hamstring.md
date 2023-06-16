## Start attack, Hamstring (put auto attack on action slot 36)
```
/cast Hamstring
/script if not IsCurrentAction(36) then UseAction(36) end;
/run if UnitMana("player") >=68 then cast("Heroic Strike") else cast("Hamstring");end
```


## Battle Stance, Charg﻿e or Hamstring i﻿f﻿ in melee ra﻿nge of the targe﻿t (put auto attack on action slot 36)
```
/script texture,name,isActive,isCastable = GetShapeshiftFormInfo(1); if isActive then CastSpellByName("Charge"); else CastSpellByName("Battle Stance"); end;
/script if not IsCurrentAction(36) then UseAction(36) end;
/cast Hamstring
```
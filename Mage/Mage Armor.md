## Mage Armor, else Frost Armor
```
/run local s="Mage" ; for i=1,16 do if strfind(UnitBuff("player",i) or "","MageArmor") then s="Frost" ; break ; end ; end ; CastSpellByName(s.." Armor"﻿)
```
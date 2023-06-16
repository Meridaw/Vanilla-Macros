## Life Tap/Demon Armo﻿r
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Shadow_RagingScream" then x=1 end i=i+1 end if x==0 then CastSpellByName("Demon Armor") else CastSpellByName("Life Tap")end
```
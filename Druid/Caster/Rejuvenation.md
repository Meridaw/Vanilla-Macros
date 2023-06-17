## Rejuvenation/Swiftmend
```
/script i=1;x=0;m=0;c=CastSpellByName;while(UnitBuff("target",i)~=nil) do if(strfind(UnitBuff("target",i),"Spell_Nature_Rejuvenation")) then m=1;end;i=i+1;end;if (m~=1) then c"Rejuvenation";else c"Swiftmend";end;﻿
```
 

## Rejuvenatio/healing Touch

If you have this on your bar instead of rejuvination, you will NEVER replace another druid's (or your own) rejuv, conserving mana and making you a more efficient healer.
```
/script i=1;x=0;m=0;c=CastSpellByName;while(UnitBuff("target",i)~=nil) do if(strfind(UnitBuff("target",i),"Spell_Nature_Rejuvenation")) then m=1;end;i=i+1;end;if (m~=1) then c"Rejuvenation";else c"Healing Touch(rank 3)";end;
```


## Rejuvenation self cast without losing target
```
/run CastSpellByName("Rejuvenation",1)
```


## Rejuvenation overwrite prevention
```
/run m=0 for i=1,40 do if(strfind(tostring(UnitBuff("target",i)),"Spell_Nature_Rejuvenation"))then m=1 end end if m==0 then CastSpellByName("Rejuvenation")end
```

 
## Rejuvenation / Swiftmend Combo
```
/run c=CastSpellByName m=0 for i=1,40 do if(strfind(tostring(UnitBuff("target",i)),"Spell_Nature_Rejuvenation"))then m=1 end end if m==0 then c("Rejuvenation") else c("Swiftmend")end
```
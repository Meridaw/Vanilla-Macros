## Turn Autogrowl on
```
/ru﻿n local i,g=1,0 while GetSpellName(i,"pet") do if GetSpellName(i,"pet")=="Growl" then g=i end i=i+1 end local _,y = GetSpellAutocast(g,"pet") if not y then ToggleSpellAutocast(g,"pet") end
```
 

## Turn Autogrowl off
```
/run local i,g=1,0 while GetSpellName(i,"pet") do if GetSpellName(i,"pet")=="Growl" then g=i end i=i+1 end local _,y = GetSpellAutocast(g,"pet") if y then ToggleSpellAutocast(g,"pet") end
```


## Disables growl whenever you tell your pet to attack a player in PvP
```
/script local i,g=1,0 while GetSpellName(i,"pet") do if GetSpellName(i,"pet")=="Growl" then g=i end i=i+1 end local _,y = GetSpellAutocast(g,"pet") if (y and UnitFactionGroup("target")) then ToggleSpellAutocast(g,"pet") end
/script PetAttack();
```
## Portal
```
/run if IsAltKeyDown() then CastSpellByName("Portal: Stormwind") elseif IsControlKeyDown() then CastSpellByName("Portal: Darnassus") else CastSpellByName("Portal: Ironforge") end
```
 

## Teleport
```
/run if IsAltKeyDown() then CastSpellByName("Teleport: Stormwind") elseif IsControlKeyDown() then CastSpellByName("Teleport: Darnassus") else CastSpellByName("Teleport: Ironforge") end
```
 

## Teleport when solo and portal when in group
```
/run if GetNumPartyMembers()==0 and GetNumRaidMembers()==0 then CastSpellByName("Teleport: Ironforge") else CastSpellByName("Portal: Ironforge") end
```
 

## Combined together
```
/run local a,b="Portal: ","Ironforge"; if GetNumPartyMembers()==0 and GetNumRaidMembers()==0 then a="Teleport: " end; if IsAltKeyDown() then b="Stormwind" elseif IsControlKeyDown() b="Darnassus" end; CastSpellByName(a..b);
```
 

Macros by Garkin
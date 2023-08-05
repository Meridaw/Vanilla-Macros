## Toggle on / off player names
```
/run if ( GetCVar("UnitNamePlayer") == "1" ) then SetCVar("UnitNamePlayer",0) else SetCVar("UnitNamePlayer",1) end
```


## Toggle on / off NPC names
```
/run if ( GetCVar("UnitNameNPC") == "1" ) then SetCVar("UnitNameNPC",0) else SetCVar("UnitNameNPC",1) end
```


## Toggle NPC names
```
/run local n="UnitNameNPC"local x=1-GetCVar(n)SetCVar(n,x)SetCVar("UnitNameFriendlyPetName",x)SetCVar("UnitNameEnemyPlayerName",x)
```


## Toggle Pet name
```
/run if PetName then if PetName:IsVisible() then PetName:Hide() else PetName:Show() end end
```
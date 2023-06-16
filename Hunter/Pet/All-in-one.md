## Call Pet, Revive Pet or Mend Pet
```
/run if not UnitExists("pet") then CastSpellByName("Call Pet") else if UnitIsDead("pet") then CastSpellByName("Revive Pet") else CastSpellByName("Mend Pet") end end
```


## Call/dismiss/revive/heal/feed
```
/run c=CastSpellByName p="pet" h=UnitHealth(p)if not UnitExists(p)then c("Call Pet")elseif h<1 then c("Revive Pet")elseif GetPetHappiness()<3 then c("Feed Pet")PickupContainerItem(3, 12)elseif h<UnitHealthMax(p)then c("Mend Pet")else c("Dismiss Pet")end
```


## Feeds, Dismisses, Calls or Revives Pet according to whatever is appropriate
```
/run local c=CastSpellByName if UnitExists("pet") then if UnitHealth("pet")==0 then c("Revive Pet") elseif GetPetHappiness()~=nil and GetPetHappiness()~=3 then c("Feed Pet") PickupContainerItem(3, 1) else c("Dismiss Pet") end else c("Call Pet") end
```
The bags are numbered starting at 0 for the blizzard bag 1, 2 3 4 for the remaining. So if you wanted to use the first slot in the blizzard bag you would change (3,1) to "(0, 1)" or if you wanted to use the 2nd slot in the 3rd bag it would be "(2, 2)"
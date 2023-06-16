## Pamper Pet
```
/run if HasPetUI() then if UnitIsDead('pet') then CastSpellByName('Revive Pet') elseif (UnitHealth('pet')/UnitHealthMax('pet')*100)<75 then CastSpellByName('Mend Pet') else CastSpellByName('Feed Pet') PickupContainerItem(0,1) end end
```

If your pet is dead, cast Revive Pet. This is the first thing the macro will do we cannot do anything with a dead pet. If your pet is alive but is significantly hurt (if the pet has lees than 75% hp), cast Mend Pet. I determined that 75% of max health is the best indicator of a pet engaged in combat, or leaving combat. Anything less, and your pet is likely on it's way to death and Mend Pet will not prevent that. Any higher, and it is a wasted Mend Pet given pets regenerate so sufficiently. If your pet is alive and healthy then Pamper Pet will cast Feed Pet and automatically grab the first item in your Backpack, so make sure you keep your pets favorite foods there and this macro is super convenient.
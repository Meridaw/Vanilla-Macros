## Adjust the automatic casting of pet based on target
```
/script PetAttack() local x,p,j,e,_={1,1,1},UnitPowerType("target");if UnitIsPlayer("target") then if p==0 then x={nil,1,1};else x={nil,1,1};end;end;for j=4,7 do _,_,_,_,_,_,e=GetPetActionInfo(j);if x[j-3]~=e then TogglePetAutocast(j);end;end;
```
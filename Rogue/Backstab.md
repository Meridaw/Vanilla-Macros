## Start attack, Backstab
```
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z);end;end;end;
/cast Backstab
```
 

## Backstab / Eviscerate
Start attack, Backstab until 5 combo points then use Eviscerate
```
/run for z=1,172 do if IsAttackAction(z) then if not IsCurrentAction(z) then UseAction(z) elseif GetComboPoints()>=5 then CastSpellByName("Eviscerate") else CastSpellByName("Backstab") end end end UIErrorsFrame:Hide()
```
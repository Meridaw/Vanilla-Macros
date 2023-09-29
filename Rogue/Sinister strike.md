## Start attack, Sinister strike
```
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z);end;end;end;
/cast Sinister Strike
```
 

## Start attack, Sinister strike until 5 combo points then use Eviscerate
```
/run for z=1,172 do if IsAttackAction(z) then if not IsCurrentAction(z) then UseAction(z) elseif GetComboPoints()>=5 then CastSpellByName("Eviscerate") else CastSpellByName("Sinister Strike") end end end UIErrorsFrame:Hide()
```
 

## Auto targeting, start attack, Sinister strike until 5 combo points then use Eviscerate (put auto attack in action slot 25)
```
/script if GetUnitName("target")==nil then TargetNearestEnemy() end if not IsCurrentAction(25) then UseAction(25) end if GetComboPoints()>=5 then CastSpellByName("Eviscerate") else CastSpellByName("Sinister Strike") end
```
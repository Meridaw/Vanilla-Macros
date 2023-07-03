## Rip / Claw / Auto attack
```
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z) elseif GetComboPoints()>=3 then CastSpellByName("Rip") else CastSpellByName("Claw") end;end;end UIErrorsFrame:Clear()
```


## Rip/Rake
```
/run if ( GetComboPoints() >= 3 ) then CastSpellByName("Rip"); else if (UnitMana("player") >= 40 ) then CastSpellByName("Rake")end end
```
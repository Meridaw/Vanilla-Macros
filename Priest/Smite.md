## Smite / Auto Attack
```
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z);end;end;end; CastSpellByName("Smite") UIErrorsFrame:Clear()
```


## Smite / Heal
```
/run if UnitCanAttack("player","target") == 1 then CastSpellByName("Smite") else CastSpellByName("Heal") end
```
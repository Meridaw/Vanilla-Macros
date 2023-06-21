## Charge
Charge if not in combat. Start auto attack. Clear melee spam.
```
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z)elseif not UnitAffectingCombat("player") then CastSpellByName("Battle Stance"); CastSpellByName("Charge")end end end UIErrorsFrame:Clear()
```
## Stop healing if target has 80% or more
Stops healing automatically if the target has 80% health or more.
```
/script if CastingBarFrame:IsShown() and UnitHealth("target")/UnitHealthMax("target") > 0.8 then SpellStopCasting() elseif not CastingBarFrame:IsShown() then CastSpellByName("Flash Heal(Rank 6)") end
```
 

## Stop healing if target has 80% hp , else Flash Heal rank 7
```
/script if CastingBarFrame:IsShown() and UnitHealth("target") / ( UnitHealthMax("target") / 100 ) > 80 then SpellStopCasting() elseif not CastingBarFrame:IsShown() then CastSpellByName("Flash Heal(Rank 7)") end
```


## Stop healing if target hp is fine, else Flash heal rank 7
```
/script if CastingBarFrame.casting and UnitHealthMax("target") - UnitHealth("target") < 1000 then SpellStopCasting() else CastSpellByName("Flash Heal(Rank 7)") end
```
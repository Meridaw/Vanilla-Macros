## Stops healing automatically if the target has 80% health or more 
change value to whatever suites you best 70/80/90 % ,.....
```
/script if CastingBarFrame:IsShown() and UnitHealth("target")/UnitHealthMax("target") > 0.8 then SpellStopCasting() elseif not CastingBarFrame:IsShown() then CastSpellByName("Lesser Healing Wave(Rank 6)") end
```
 

## Stopcasting if target has more then 80%hp, else Healing wave
```
/script if CastingBarFrame:IsShown() and UnitHealth("target")/UnitHealthMax("target") > 0.8 then SpellStopCasting() elseif not CastingBarFrame:IsShown() then CastSpellByName("Healing Wave(Rank 6)") end
```
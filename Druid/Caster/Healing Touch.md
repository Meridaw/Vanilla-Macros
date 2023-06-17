## Stopcast if target has more then 80%hp, else Healing Touch
```
/script if CastingBarFrame:IsShown() and UnitHealth("target")/UnitHealthMax("target") > 0.8 then SpellStopCasting() elseif not CastingBarFrame:IsShown() then CastSpellByName("Healing Touch(Rank 6)") end
```
 

## Smart Touch
```
/script r=10;H=UnitHealthMax("target")-UnitHealth("target");SR={140,350,640,1100,1500,1799,2004,2385,2600,3100};for i=r,1,-1 do if (H>(SR)) then CastSpellByName("Healing Touch(Rank "..i..")");break;end;end;
```
 

## Wrath/Healing Touch
```
/run if UnitCanAttack("player","target") == 1 then CastSpellByName("Wrath") else CastSpellByName("Healing Touch") end
```
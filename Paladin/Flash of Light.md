## Stopcasting if target has more then 80%hp, else Flash of Light
```
/script if CastingBarFrame:IsShown() and UnitHealth("target")/UnitHealthMax("target") > 0.8 then SpellStopCasting() elseif not CastingBarFrame:IsShown() then CastSpellByName("Flash of Light(Rank 4)") end
```
 

## Flash of Light/SpellStopCasting
```
/run if (UnitHealth('target')/UnitHealthMax('target')>0.99) then SpellStopCasting() end
/cast Flash of Light(Rank 4)
```
 

## Flash of Light nearest target
```
/run for i=1,40 do TargetNearestFriend() if UnitHealth("target")/UnitHealthMax("target") < 0.9 then if UnitIsPlayer("target") then CastSpellByName("Flash of Light") end end end
```
 

## Heals you based on how much hp missing
```
/run x="player";d=UnitHealthMax(x)-UnitHealth(x);if (d>200) then if (d<400) then CastSpellByName("Flash of Light(Rank 3)") else CastSpellByName("Holy Light(Rank 5)") end;SpellTargetUnit(x);else DEFAULT_CHAT_FRAME:AddMessage("Health is good"); end;
```
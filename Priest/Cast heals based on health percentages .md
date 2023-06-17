## Rank 1 Flash Heal / Rank 3 Flash Heal
This one cast Rank 1 until the target is under 50% health, then cast Rank 3. Adjustments can be made to the percentage. 
```
/script if(UnitHealth("target")/UnitHealthMax("target")<0.50) then CastSpellByName("Flash Heal(Rank 3)")else CastSpellByName("Flash Heal(Rank 1)"); end
```
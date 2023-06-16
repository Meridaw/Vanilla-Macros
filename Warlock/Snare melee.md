## Snare melee classes and Curse of Shadow everyone else
```
/run local c,u=CastSpellByName,UnitClass('target') if u == 'Druid' then c('Curse of Shadow') elseif UnitPowerType('target') ~= 0 or u == 'Paladin' then c('Curse of Exhaustion') else c('Curse of Shadow') end
```
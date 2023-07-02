## Conjure Water
Conjure Water for yourself and friendly targets based on level
```
/run r=7;l={1,5,15,25,35,45,55};if not UnitIsFriend("player","target")then TargetUnit("player");end;t=UnitLevel("target");for i=r,1,-1 do if (t>=l[ i]) then CastSpellByName("Conjure Water(Rank "..i..")");break;end;end
```
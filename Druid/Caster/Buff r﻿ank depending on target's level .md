## Regrowth
```
/script r=9;l={12,18,24,30,36,42,48,54,60};if not UnitIsFriend("player","target")thenTargetUnit("player");end;t=UnitLevel("target");for i=r,1,-1 do if (t>=l-10) thenCastSpellByName("Regrowth(Rank "..i..")");break;end;end
```
 

## Rejuvenation
```
/script r=10;l={4,10,16,22,28,34,40,46,52,58};if not UnitIsFriend("player","target")thenTargetUnit("player");end;t=UnitLevel("target");for i=r,1,-1 do if (t>=l-10) thenCastSpellByName("Rejuvenation(Rank "..i..")");break;end;end
```
 

## Mark of the Wild
```
/script r=7;l={1,10,20,30,40,50,60};if not UnitIsFriend("player","target")thenTargetUnit("player");end;t=UnitLevel("target");for i=r,1,-1 do if (t>=l-10) thenCastSpellByName("Mark of the Wild(Rank "..i..")");break;end;end
```
 

## Thorns
```
/script r=6;l={6,14,24,34,44,54};if not UnitIsFriend("player","target")thenTargetUnit("player");end;t=UnitLevel("target");for i=r,1,-1 do if (t>=l-10) thenCastSpellByName("Thorns(Rank "..i..")");break;end;end
```
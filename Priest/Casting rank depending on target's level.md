## Fortitude
```
/run local a,b,c,d,e,u="Power Word: Fortitude",{1,10,20,30,40,50},"target","(Rank ",CastSpellByName,UnitLevel if u(c)~=nil and UnitIsFriend("player",c)then for i=6,1,-1 do if(u(c)>=b)then e(a..d..i..")")return end end else e(a,1) end
```
 

## Shield
```
/run local a,b,c,d,e,u="Power Word: Shield",{1,6,12,18,24,30,36,42,48,54},"target","(Rank ",CastSpellByName,UnitLevel if u(c)~=nil and UnitIsFriend("player",c)then for i=10,1,-1 do if(u(c)>=b)then e(a..d..i..")")return end end else e(a,1) end
```
 

## Shadow Protection
```
/script r=3;l={30,42,56};if not UnitIsFriend("player","target")then TargetUnit("player");end;t=UnitLevel("target");for i=r,1,-1 do if (t>=l-10) then CastSpellByName("Shadow Protection(Rank "..i..")");break;end;end;
```
 

## Renew
```
/script r=9;l={8,14,20,26,32,38,44,50,56};if not UnitIsFriend("player","target")then TargetUnit("player");end;t=UnitLevel("target");for i=r,1,-1 do if (t>=l-10) then CastSpellByName("Renew(Rank "..i..")");break;end;end;
```
 

## Divine Spirit
```
/script r=4;l={20,28,38,48};if not UnitIsFriend("player","target")then TargetUnit("player");end;t=UnitLevel("target");for i=r,1,-1 do if (t>=l) then CastSpellByName("Divine Spirit(Rank "..i..")");break;end;end;
```
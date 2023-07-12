## Mouseover dispel
```
/run if UnitExists("mouseover") then TargetUnit("mouseover"); CastSpellByName("Dispel Magic"); TargetUnit("playertarget") else CastSpellByName("Dispel Magic") end
```


## Dispel Magic from target if target is a player, else Dispel Magic from oneself
```
/run if UnitIsFriend("player","target") then CastSpellByName("Dispel Magic") else CastSpellByName("Dispel Magic",1)  end; TargetLastEnemy();
```
 

## Dispel self-cast modifier 
replace IsAltKeyDown() with IsShiftKeyDown() or IsControlKeyDown() if you want to use another modifier
```
/run if IsAltKeyDown()then CastSpellByName("Dispel Magic",1)else CastSpellByName("Dispel Magic")end
```
 

## Dispel Raid
```
/run local s,p,i,d,t,_={["Magic"]="Dispel Magic",["Disease"]="Abolish Disease"};for i=1,40 do p="raid"..i;if CheckInteractDistance(p,4) then d,_,t=UnitDebuff(p,1);if d then TargetUnit(p);CastSpellByName(s[t]);TargetLastTarget();break;end;end;end
```
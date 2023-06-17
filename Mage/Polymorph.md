## Mouseover Polymorph without changing target
```
/run c=CastSpellByName s="Polymorph(Rank 4)" if UnitExists("mouseover") then TargetUnit("mouseover") c(s) TargetLastTarget() else c(s) end
```
You can replace s=”mySpellName(Rank X)” with any other spell of you’re choice.

 

## Polymorph turtle:   
```
/run c=CastSpellByName s="Polymorph: Turtle" if UnitExists("mouseover") then TargetUnit("mouseover") c(s) TargetLastTarget() else c(s) end
```
 

Alternative less compact version if you want it to register cooldowns etc using Addons like Bongos.   
```
/run if UnitExists("mouseover") then TargetUnit("mouseover") CastSpellByName("Polymorph(Rank 4)") TargetLastTarget() else CastSpellByName("Polymorph(Rank 4)") end
```
 

## Sheep controlled teammates (BWL Nefarian, ZG Hakkar)
```
/run local n,p,i,t=4,"party";if UnitInRaid("player") then n=40;p="raid";end;for i=1,n do t=p..i ;if UnitCanAttack("player",t) then TargetUnit(t);CastSpellByName("Polymorph");SendChatMessage("%t is controlled, I changed him to sheep~",p);break;end;end
```
 

## Polymorph rank 1 if target is player controlled, else max rank
```
/run if UnitPlayerControlled("target") then CastSpellByName("Polymorph(Rank 1)")else CastSpellByName("Polymorph")end
```
 

## Polymorph and message party and raid
Casts polymorph, and searches through the party and raid for anyone who is targeting what you are going to polymorph, and whispering them to change targets.
```
/cast Polymorph
/run n,s=UnitName,UnitIsUnit;y,p,r,t="player","raid","party","target";for i=1,40 do a=((n(r..i)and r..i)or(n(p..i) and p..i)or nil);z=a and(not s(a,y)) and s(a..t,t) and SendChatMessage("Sheeping your: "..n(t),"WHISPER",nil,n(a))end
``` 
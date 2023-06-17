## Uses any bandage without losing target
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Bandage"))then UseContainerItem(b,s)SpellTargetUnit("player")end end end
```
 

## Bandage without losing target 
Put bandage in action slot 53
```
/script p="player";t="target";if(not UnitCanAttack(t, p))then ot=UnitName(t);TargetUnit(p); else ot=nil;end;UseAction(53);if(SpellIsTargeting())then SpellTargetUnit(p); end if(ot) then TargetByName(ot);end
```
 

## Bandage self, then TargetLastTarget 
Put bandage in action slot 47
```
/run UseAction(47) SpellTargetUnit("player") local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\INV_Misc_Bandage_08" then x=1 end i=i+1 end if x==1 then TargetLastTarget()end
```
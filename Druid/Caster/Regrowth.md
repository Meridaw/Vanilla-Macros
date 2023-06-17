## Unshift+Regrowth self/target
```
/run local c,r,a,_=CastSpellByName,"Regrowth";for i=1,GetNumShapeshiftForms()do _,_,a=GetShapeshiftFormInfo(i)if(a)then CastShapeshiftForm(i)break end end if UnitIsFriend("player","target")then c(r)else c(r,1)end
```
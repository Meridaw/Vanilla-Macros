## Unshift + cat + dash
``` 
/run local f=0 for i=1,GetNumShapeshiftForms()do if({GetShapeshiftFormInfo(i)})[3]then f=i end end if f ~= 0 and f ~= 3 then CastShapeshiftForm(f) else if f == 3 then CastSpellByName("Dash") else CastShapeshiftForm(3) end end
``` 
 

## Unshift + cat + prowl
``` 
/run local f=0 for i=1,GetNumShapeshiftForms()do if({GetShapeshiftFormInfo(i)})[3]then f=i end end if f ~= 0 and f ~= 3 then CastShapeshiftForm(f) else if f == 3 then CastSpellByName("Prowl") else CastShapeshiftForm(3) end end
``` 
## Travel Form
``` 
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Ability_Druid_TravelForm" then x=1 end i=i+1 end if x==0 then CastSpellByName("Travel Form") else end
``` 


## Aquatic / Travel Form
``` 
/run UIErrorsFrame:UnregisterEvent"UI_ERROR_MESSAGE" for i = 2, GetNumShapeshiftForms(), 2 do local _, _, active = GetShapeshiftFormInfo(i) if not active then CastShapeshiftForm(i) end if i == 2 then UIErrorsFrame:RegisterEvent"UI_ERROR_MESSAGE" end end
``` 
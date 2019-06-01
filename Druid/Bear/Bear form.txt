Bear Form from any form, 2 clicks.

/script local s,_ for i=1,5 do _,_,s=GetShapeshiftFormInfo(i)if s then CastShapeshiftForm(i)break end end if not s then CastShapeshiftForm(1) end
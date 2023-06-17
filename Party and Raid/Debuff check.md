## Check what important debuff is missing on the raid boss
```
/run str=UnitName("target") b=UnitExists("target") CoS=false for i=1,16,1 do db=UnitDebuff("target",i) if(db~=nil and string.find(db,"Spell_Shadow_CurseOfAchimonde")) then CoS=true end end;
/run if CoS then print("COS true") else if b then str=str .. " has no Curse Of Shadow!" end end;
/run CoE=false for i=1,16,1 do db=UnitDebuff("target",i) if(db~=nil and string.find(db,"Spell_Shadow_ChillTouch")) then CoE=true end end;
/run if CoE then print("COE true") else if b then str=str .. " has no Curse of Elements!" end end;
/run CoR=false for i=1,16,1 do db=UnitDebuff("target",i) if(db~=nil and string.find(db,"Spell_Shadow_UnholyStrength")) then CoR=true end end;  
/run FF=false for i=1,16,1 do db=UnitDebuff("target",i) if(db~=nil and string.find(db,"Spell_Nature_FaerieFire")) then FF=true end end;  
/run if CoR then print("COR true") else if b then str=str .. " has no Curse Of Recklessness!" end end;
/run if FF then print("FF true") else if b then str=str .. " has no Faerie Fire!" end end;
/run --SW=false for i=1,16,1 do db=UnitDebuff("target",i) if(db~=nil and string.find(db,"Spell_Shadow_BlackPlague")) then SW=true end end;
/run --if SW then print("SW true") else if b then str=str .. " has no Shadow Weaving!" end end;
/run SendChatMessage(str, "yell") --made by Imwithstupid ﻿
```
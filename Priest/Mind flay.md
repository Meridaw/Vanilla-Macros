## Spammable Mind Flay
Using Mind Flay repeatedly is a DPS loss because of the way the spell works, so you need this complicated macro to gain an extra tick of the spell
```
/run local f=CnlSpam if not f then f=CreateFrame("Frame")local s,r="SPELLCAST_CHANNEL_ST",f.RegisterEvent r(f,s.."ART")r(f,s.."OP")f:SetScript("OnEvent",function()this.c=event~=s.."OP"end)CnlSpam=f end if not f.c then CastSpellByName("Mind Flay")end
```


## Spammable Mind Flay
```
/run if not CastingBarFrame.channeling then CastSpellByName("Mind Flay") end
```


## Time-based Mind Flay
time-based. first click will set the castTime variable and then cast the spell on the next click. 
```
/run castTime = 3 if not casting then CastSpellByName("Mind Flay") casting = true startTime = GetTime() end if casting and GetTime() > startTime + castTime then casting = false end
```

 
## Check if Mind Flay (Rank 6)
This macro will cast rank 6 Mind Flay if your current target is not already a victim to the spell.
```
/run m=0 for i=1,40 do if(strfind(tostring(UnitDebuff("target",i)),"Spell_Shadow_SiphonMana"))then m=1 end end if m==0 then CastSpellByName("Mind Flay(Rank 6)") end
```


## Check if Mind Flay
This macro will cast Mind Flay if your current target is not already a victim to the spell.
```
/run while nil do CastSpellByName"Mind Flay" end
/run k=0 local i=1 while UnitBuff("target",i) ~= nil do if string.find(UnitBuff("target",i),"Shadow_SiphonMana") then k=1 end i=i+1 end if k==0 then CastSpellByName"Mind Flay" end
``` 
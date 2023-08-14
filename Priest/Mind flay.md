## Mind Flay
```
/run if not CastingBarFrame.channeling then CastSpellByName("Mind Flay") end
```

## Mind Flay
time-based. first click will set the castTime variable and then cast the spell on the next click. 
/run castTime = 3 if not casting then CastSpellByName("Mind Flay") casting = true startTime = GetTime() end if casting and GetTime() > startTime + castTime then casting = false end

 
## Mind Flay Rank 6
This macro will cast rank 6 Mind Flay if your current target is not already a victim to the spell.
```
/run m=0 for i=1,40 do if(strfind(tostring(UnitDebuff("target",i)),"Spell_Shadow_SiphonMana"))then m=1 end end if m==0 then CastSpellByName("Mind Flay(Rank 6)") end
```


## Mind Flay
This macro will cast Mind Flay if your current target is not already a victim to the spell.
```
/run while nil do CastSpellByName"Mind Flay" end
/run k=0 local i=1 while UnitBuff("target",i) ~= nil do if string.find(UnitBuff("target",i),"Shadow_SiphonMana") then k=1 end i=i+1 end if k==0 then CastSpellByName"Mind Flay" end
``` 
## Far Sight
```
/run if CastingBarFrame.channeling then if n~=1 then CancelPlayerBuff(GetPlayerBuff(0,"HELPFUL")) CancelPlayerBuff(GetPlayerBuff(1,"HELPFUL"))  n=1 else CastSpellByName("Far Sight") n=0 ;end; else CastSpellByName("Far Sight") end
```
## Seal of Light + Judgement
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Holy_HealingAura" then x=1 end i=i+1 end if x==0 then CastSpellByName("Seal of Light") else CastSpellByName("Judgement")end
```

## Spammable Light
Seal of light that cannot be reapplied while buff is up
```
/run i=0;s=0;while(1) do b=GetPlayerBuff(i,"HELPFUL") if b==-1 then break;end t=GetPlayerBuffTexture(b); if string.find(t,"HealingAura") then s=1;end i=i+1;end if s==0 or IsControlKeyDown() then CastSpellByName("Seal of Light"); end
```
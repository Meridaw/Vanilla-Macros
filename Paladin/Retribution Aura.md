## Spammable Retribution Aura
```
/run i=0;s=0;while(1) do b=GetPlayerBuff(i,"HELPFUL") if b==-1 then break;end t=GetPlayerBuffTexture(b); if string.find(t,"AuraOfLight") then s=1;end i=i+1;end if s==0 then CastSpellByName("Retribution Aura");end
```
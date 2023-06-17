## Tiger’s Fury, Ravage
``` 
/run i=0 m=0 c=CastSpellByName while not (GetPlayerBuff(i)==-1) do if (strfind(GetPlayerBuffTexture(GetPlayerBuff(i)),"Ability_Mount_JungleTiger")) then m=1 end i=i+1 end if m==0 then c("Tiger's Fury") else c("Ravage") end
``` 
 

## Spammable Tiger’s Fury
``` 
/run i=0 m=0 c=CastSpellByName while not (GetPlayerBuff(i)==-1) do if (strfind(GetPlayerBuffTexture(GetPlayerBuff(i)),"Ability_Mount_JungleTiger")) then m=1 end i=i+1 end if m==0 then c("Tiger's Fury") end
```
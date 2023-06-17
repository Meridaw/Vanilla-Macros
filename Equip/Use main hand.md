## Use main hand if Haste effect from Crowd Pummeler is missing
```
/run i=0 m=0 while not (GetPlayerBuff(i)==-1) do if (strfind(GetPlayerBuffTexture(GetPlayerBuff(i)),"Spell_Nature_Invisibilty")) then m=1 end i=i+1 end if m==0 then UseInventoryItem(16); end
```
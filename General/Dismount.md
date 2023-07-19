## Dismount
```
/run local i=0 g=GetPlayerBuff while not(g(i) == -1)do if(strfind(GetPlayerBuffTexture(g(i)), "Ability_Mount"))then CancelPlayerBuff(g(i))end i=i+1 end
```
## Max rank Divine Protection 
cast + unbuff max rank Divine Protection
```
/cast Divine Protection
/script local i=0 g=GetPlayerBuff while not (g(i) == -1) do if(strfind(GetPlayerBuffTexture(g(i)), "Spell_Holy_Restoration"))then CancelPlayerBuff(g(i))end i = i + 1; end
```
 

## Rank 1 Divine Protection 
cast + unbuff rank 1 Divine Protection
```
/script local i=0 g=GetPlayerBuff while not (g(i) == -1) do if (strfind(GetPlayerBuffTexture(g(i)), "Spell_Holy_Restoration")) then CancelPlayerBuff(g(i)) end i = i + 1; end
/cast Divine Protection(Rank 1)
``` 
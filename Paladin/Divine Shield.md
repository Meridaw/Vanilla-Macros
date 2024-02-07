## Max rank Divine Shield 
cast + unbuff max rank Divine Shield
```
/cast Divine Shield
/script local i=0 g=GetPlayerBuff while not (g(i) == -1) do if(strfind(GetPlayerBuffTexture(g(i)), "Spell_Holy_DivineIntervention"))then CancelPlayerBuff(g(i))end i = i + 1; end
```
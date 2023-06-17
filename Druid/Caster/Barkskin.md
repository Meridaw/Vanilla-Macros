## Barkskin + cancel buff
```
/run local i=0 g=GetPlayerBuff while not (g(i) == -1) do if(strfind(GetPlayerBuffTexture(g(i)),"Spell_Nature_StoneClawTotem"))then CancelPlayerBuff(g(i)) end i = i + 1; end; CastSpellByName("Barkskin")
```
## Buff Slow Fall, or cancel buff
```
/script CastSpellByName("Slow Fall")
/script local i=0 g=GetPlayerBuff while not(g(i) == -1)do if(strfind(GetPlayerBuffTexture(g(i)), "Spell_Magic_FeatherFall"))then CancelPlayerBuff(g(i))end i=i+1 end
```
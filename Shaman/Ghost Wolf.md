## Cancel Ghost Wolf
```
/run local i=0 g=GetPlayerBuff while not(g(i) == -1)do if(strfind(GetPlayerBuffTexture(g(i)), "SpiritWolf"))then CancelPlayerBuff(g(i))end i=i+1 end
```


## Cancel Ghost Wolf, cast Healing Wave on self
```
/run local i=0 g=GetPlayerBuff while not(g(i) == -1)do if(strfind(GetPlayerBuffTexture(g(i)), "SpiritWolf"))then CancelPlayerBuff(g(i))end i=i+1 end CastSpellByName("Healing Wave",1)
```
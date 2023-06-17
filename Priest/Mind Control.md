## Mind Control target, then use attack and spells
```
/run if not CastingBarFrame.channeling then CastSpellByName("Mind Control");end CastPetAction(1);CastPetAction(2);CastPetAction(3);
```


## Cancel Mind Control
```
/run local i=0 g=GetPlayerBuff while not(g(i) == -1)do if(strfind(GetPlayerBuffTexture(g(i)), "Spell_Shadow_ShadowWordDominate"))then CancelPlayerBuff(g(i))end i=i+1 end
```
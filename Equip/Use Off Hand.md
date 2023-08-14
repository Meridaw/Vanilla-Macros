## Use offhand
```
/script UseInventoryItem(17);
```


## Use offhand / cancel Skull of Impending Doom effect
```
/script UseInventoryItem(17);
/run SpellStopCasting()
/script local i=0 g=GetPlayerBuff while not(g(i) == -1)do if(strfind(GetPlayerBuffTexture(g(i)), "Spell_Magic_PolymorphChicken"))then CancelPlayerBuff(g(i))end i=i+1 end
```
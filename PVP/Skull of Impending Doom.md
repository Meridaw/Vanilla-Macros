## Use offhand or cancel buff
```
/script UseInventoryItem(17);
/run SpellStopCasting()
/script local i=0 g=GetPlayerBuff while not(g(i) == -1)do if(strfind(GetPlayerBuffTexture(g(i)), "Spell_Magic_PolymorphChicken"))then CancelPlayerBuff(g(i))end i=i+1 end
```
You can also swap the offhand to remove this buff 
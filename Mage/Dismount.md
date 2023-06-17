## Dismount, Blink (put mount in action slot 60)
```
/script SpellStopCasting()
/script CastSpellByName("Blink")
/run i=1 while UnitBuff("player",i) do if string.find(UnitBuff("player",i),"Mount") then UseAction(60)end i=i+1 end
```
 

## Dismount, Sheep
```
/run CastSpellByName("Polymorph")
/run local i=0 g=GetPlayerBuff while not(g(i) == -1)do if(strfind(GetPlayerBuffTexture(g(i)), "Mount"))then CancelPlayerBuff(g(i))end i=i+1 end
```
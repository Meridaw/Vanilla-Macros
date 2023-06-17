## Dismount, Power Word: Shield
```
/run CastSpellByName("Power Word: Shield")
/run local i=0 g=GetPlayerBuff while not(g(i) == -1)do if(strfind(GetPlayerBuffTexture(g(i)), "Mount"))then CancelPlayerBuff(g(i))end i=i+1 end
```
 

## Dismount, Shadow Word: Pain 
put mount in action slot 60 for the macro to work
```
/run CastSpellByName("Shadow Word: Pain")
/run i=1 while UnitBuff("player",i) do if string.find(UnitBuff("player",i),"Mount") then UseAction(60)end i=i+1 end
```
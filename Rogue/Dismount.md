## Dismount, Stealth, Cheap shot (put mount in action slot 58)
```
/script a,b,c=GetShapeshiftFormInfo(1);if (c) then CastSpellByName("Cheap Shot") else CastSpellByName("Stealth");end
/run i=1 while UnitBuff("player",i)do if string.find(UnitBuff("player",i),"Mount")then UseAction(58)end i=i+1 end
```
 

## Dismount, Stealth, Cheap shot
```
/run a,b,c=GetShapeshiftFormInfo(1);if (c) then CastSpellByName("Cheap Shot")else CastSpellByName("Stealth")end
/run local i=0 g=GetPlayerBuff while not(g(i) == -1)do if(strfind(GetPlayerBuffTexture(g(i)), "Mount"))then CancelPlayerBuff(g(i))end i=i+1 end
```


## Dismount, Stealth, else Sap (put mount in action slot 26)
```
/run a,b,c=GetShapeshiftFormInfo(1);if c then TargetNearestEnemy() CastSpellByName("Sap") else CastSpellByName("Stealth");end
/run i=1 while UnitBuff("player",i) do if string.find(UnitBuff("player",i),"Mount") then UseAction(26)end i=i+1 end
```
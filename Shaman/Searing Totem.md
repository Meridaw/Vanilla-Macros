## Start attack, Searing Totem
```
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z);end;end;end;
/cast Searing Totem
```


## Fire Nova Totem, Searing Totem
use Fire Nova Totem and Searing Totem with a 15 second cooldown
```
/script if Ttwist == nil or (GetTime()-Ttwist>15) then Ttwist,wTot=GetTime(),true CastSpellByName("Fire Nova Totem") elseif wTot and (GetTime()-Ttwist>5) then CastSpellByName("Searing Totem"); wTot=false end
```
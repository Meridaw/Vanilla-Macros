## Fire Nova Totem, Magma Totem
use Fire Nova Totem and Magma Totem with a 15 second cooldown
```
/script if Ttwist == nil or (GetTime()-Ttwist>15) then Ttwist,wTot=GetTime(),true CastSpellByName("Fire Nova Totem") elseif wTot and (GetTime()-Ttwist>5) then CastSpellByName("Magma Totem"); wTot=false end
```


## Fire Nova Totem, Searing Totem
use Fire Nova Totem and Searing Totem with a 15 second cooldown
```
/script if Ttwist == nil or (GetTime()-Ttwist>15) then Ttwist,wTot=GetTime(),true CastSpellByName("Fire Nova Totem") elseif wTot and (GetTime()-Ttwist>5) then CastSpellByName("Searing Totem"); wTot=false end
```
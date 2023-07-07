## Spammable Windfury / Grace of Air
uses Windfury and Grace of Air with a 10 second cooldown
```
/run if Ttwist == nil or (GetTime()-Ttwist>10) then Ttwist,wTot=GetTime(),true CastSpellByName("Windfury Totem") elseif wTot and (GetTime()-Ttwist>1.5) then CastSpellByName("Grace of Air Totem"); wTot=false end
```


## Windfury / Grace of Air
```
/run if n~= 1 then CastSpellByName("Windfury Totem") n=1 else CastSpellByName("Grace of Air Totem") n=0 end
```


## Searing / Strength of Earth / Healing Stream
```
/run c=CastSpellByName if n==0 then c("Searing Totem") n=1 elseif n==1 then c("Strength of Earth Totem") n=2 else c("Healing Stream Totem") n=0 ;end
```
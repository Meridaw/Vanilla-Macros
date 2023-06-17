## Windfury / Grace of Air
```
/run if n~= 1 then CastSpellByName("Windfury Totem") n=1 else CastSpellByName("Grace of Air Totem") n=0 end
```


## Searing / Strength of Earth / Healing Stream
```
/run c=CastSpellByName if n==0 then c("Searing Totem") n=1 elseif n==1 then c("Strength of Earth Totem") n=2 else c("Healing Stream Totem") n=0 ;end
```
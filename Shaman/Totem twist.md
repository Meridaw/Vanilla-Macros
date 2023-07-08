## Spammable Windfury / Grace of Air
uses Windfury and Grace of Air with a 10 second cooldown
```
/run if Ttwist == nil or (GetTime()-Ttwist>10) then Ttwist,wTot=GetTime(),true CastSpellByName("Windfury Totem") elseif wTot and (GetTime()-Ttwist>1.5) then CastSpellByName("Grace of Air Totem"); wTot=false end
```


## Windfury / Grace of Air
```
/run if n~= 1 then CastSpellByName("Windfury Totem") n=1 else CastSpellByName("Grace of Air Totem") n=0 end
```


## Grace of Air Totem, else Windfury Totem
If you got Windfury on mainhand cast Grace of Air Totem, else Windfury Totem
```
/run hasMainHandEnchant = GetWeaponEnchantInfo() if  not hasMainHandEnchant then CastSpellByName("Windfury Totem")else CastSpellByName("Grace of Air Totem")end
```
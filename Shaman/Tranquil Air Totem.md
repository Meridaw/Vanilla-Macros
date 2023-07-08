## Spammable Windfury / Tranquil Air
uses Windfury and Tranquil Air Totem with a 10 second cooldown
```
/run if Ttwist == nil or (GetTime()-Ttwist>10) then Ttwist,wTot=GetTime(),true CastSpellByName("Windfury Totem") elseif wTot and (GetTime()-Ttwist>1.5) then CastSpellByName("Tranquil Air Totem"); wTot=false end
```


## Tranquil Air Totem, else Windfury Totem
If you got Windfury on mainhand cast Tranquil Air Totem, else Windfury Totem
```
/run hasMainHandEnchant = GetWeaponEnchantInfo() if  not hasMainHandEnchant then CastSpellByName("Windfury Totem")else CastSpellByName("Tranquil Air Totem")end
```
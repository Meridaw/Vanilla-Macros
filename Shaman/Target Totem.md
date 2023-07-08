## Windfury Totem
Target Windfury Totem, if in duel range (9.9 yards) target last target, else cast Windfury Totem (edit III and YOURNAME)
```
/run TargetByName("Windfury Totem III YOURNAME", exactMatch) if not CheckInteractDistance("target",3) then CastSpellByName("Windfury Totem")else TargetLastTarget()end
```


## Cast Frost Shock, else Earthbind totem
```
/cast Frost Shock
/run TargetByName("Earthbind Totem YOURNAME", exactMatch) if not CheckInteractDistance("target",3) then CastSpellByName("Earthbind Totem")else TargetLastTarget()end
```
 
 

 


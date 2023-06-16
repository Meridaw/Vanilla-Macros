## If stealthed cast Gouge, else cast Backstab
```
/script if not(string.find(GetShapeshiftFormInfo(1), "Invis" )) then CastSpellByName("Backstab") else CastSpellByName("Gouge"); end
```
 

## If target is Gouged cast Backstab, else cast Gouge
```
/run local i,x=1,0 while UnitDebuff("target",i) do if UnitDebuff("target",i)=="Interface\\Icons\\Ability_Gouge" then x=1 end i=i+1 end if x==0 then CastSpellByName("Gouge") else CastSpellByName("Backstab")end
```
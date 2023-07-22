## Track Hidden, else spammable flare
```
/run local g,h=GetTrackingTexture(),"Ability_Stealth";if not strfind(g,h) then CastSpellByName("Track Hidden")else if not SpellIsTargeting() then CastSpellByName("Flare")end end
```
 

## Hunter's Mark if target can be attacked, else Flare
```
/run if UnitCanAttack("player","target") then CastSpellByName("Hunter's Mark") else CastSpellByName("Flare") end;
```
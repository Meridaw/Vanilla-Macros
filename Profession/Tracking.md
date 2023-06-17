## Find Herbs, else Minerals
```
/run if n~= 1 then CastSpellByName("Find Herbs") n=1 else CastSpellByName("Find Minerals") n=0 ;end
```
 

## Find Minerals, else Herbs
```
/run local g,h=GetTrackingTexture(),"INV_Misc_Flower_02";if strfind(g,h)then CastSpellByName("Find Minerals")else CastSpellByName("Find Herbs")end
```
 

## Find Treasure/Minerals
```
/run local s,t,c={'Find Treasure','Find Minerals'},{'Racial_Dwarf_FindTreasure','Spell_Nature_Earthquake'},GetTrackingTexture()foreach(t,function(k,v)if not c or strfind(c,v) then CastSpellByName(k<getn(t)and s[k+1]or s[1]) end end)
```
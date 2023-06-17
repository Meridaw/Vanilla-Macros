## Cancel Ice Block, then Blink
```
/run local z=0 for i=1,27 do t=UnitBuff("player",i) if (t and string.find(t,"Frost")) then z=1 break end end if z==1 then CastSpellByName("Ice Block")end
/cast Blink
```
 

## Cancel Ice Block, then Blink
```
/script local i=0 g=GetPlayerBuff while not(g(i) == -1)do if(strfind(GetPlayerBuffTexture(g(i)), "Spell_Frost_Frost"))then CancelPlayerBuff(g(i))end i=i+1 end CastSpellByName("Blink")
```
 

## Ice Block, else cancel Ice Block, then Blink
```
/cast Ice Block
/cast Blink
```
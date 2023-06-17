## Cancel Shadowform
```
/run local i=0 g=GetPlayerBuff if not(g(i)==-1)then do if(strfind(GetPlayerBuffTexture(g(i)), "Shadowform"))then CancelPlayerBuff(g(i))end i=i+1 end end
```


## Cancel Shadowform, Flash Heal self
```
/run local i=0 g=GetPlayerBuff if not(g(i)==-1)then do if(strfind(GetPlayerBuffTexture(g(i)), "Shadowform"))then CancelPlayerBuff(g(i))end i=i+1 end end CastSpellByName("Flash Heal",1)
```


## Buff Shadowform, Inner Fire
```
/run z=false for i=1,16,1 do db=UnitBuff("player",i) if(db~=nil and string.find(db,"Shadowform")) then z=true end end if z then CastSpellByName("Inner Fire") else CastSpellByName("Shadowform") end
```

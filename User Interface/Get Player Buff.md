## Target Buff / Debuff
shows names of positive and negative effects on the target
```
/run function m(s) DEFAULT_CHAT_FRAME:AddMessage(s); end for i=1,16 do s=UnitBuff("target", i); if(s) then m("B "..i..": "..s); end s=UnitDebuff("target", i); if(s) then m("D "..i..": "..s); end end
```


## Player Buff Information
shows mainly the name of the texture
```
/run i=1; while UnitBuff("player",i)~=nil do DEFAULT_CHAT_FRAME:AddMessage(UnitBuff("player",i)); i=i+1; end
```


## Target Buff Information
check buff icons' names on current target
```
/run i=1; while UnitBuff("target",i)~=nil do DEFAULT_CHAT_FRAME:AddMessage(UnitBuff("target",i)); i=i+1; end
```
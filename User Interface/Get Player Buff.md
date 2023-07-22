## Get player buff information
Mainly the name of the texture
```
/run i=1; while UnitBuff("player",i)~=nil do DEFAULT_CHAT_FRAME:AddMessage(UnitBuff("player",i)); i=i+1; end
```


## Get target buff information
check buff icons' names on current target
```
/run i=1; while UnitBuff("target",i)~=nil do DEFAULT_CHAT_FRAME:AddMessage(UnitBuff("target",i)); i=i+1; end
```
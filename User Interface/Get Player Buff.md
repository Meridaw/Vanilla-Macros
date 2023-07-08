## Get player buff information
Mainly the name of the texture
```
/run for i=1,32 do local B=UnitBuff("player",i);if B then print(i.."="..B) end;end
```


## Get target buff information
check buff icons' names (on current target)
```
/script i=1; while UnitBuff("target",i)~=nil do DEFAULT_CHAT_FRAME:AddMessage(UnitBuff("target",i)); i=i+1; end
```
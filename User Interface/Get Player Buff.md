## Get player buff information
```
/run for i=1,32 do local B=UnitBuff("player",i);if B then print(i.."="..B) end;end
```
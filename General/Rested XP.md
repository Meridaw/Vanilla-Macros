## Show current % rested experience
```
/run DEFAULT_CHAT_FRAME:AddMessage(format("%d%% rested", 100 * GetXPExhaustion() / UnitXPMax("player")))
```
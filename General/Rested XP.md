## Show current % rested experience
```
/run DEFAULT_CHAT_FRAME:AddMessage(format("%d%% rested", 100 * GetXPExhaustion() / UnitXPMax("player")))
```


## Rested xp macro
```
/run p="player";x=UnitXP(p);m=UnitXPMax(p);r=GetXPExhaustion();if -1==(r or -1)then t="No rest."else t="Rest: "..(math.floor(20*r/m+0.5)).."bubbles ("if r+x<m then t=t..r else t=t.."level +"..(r+x-m)end t=t.."XP)"end;DEFAULT_CHAT_FRAME:AddMessage(t)
```
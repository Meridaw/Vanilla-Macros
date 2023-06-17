## Calculate RP
```
/run P=(math.floor(GetPVPRankProgress(target)*10000))/100 W=UnitPVPRank("player") N=(W-6)*5000+5000*P/100 Q=(W-5)*5000-N*0.8 SendChatMessage("Rank Progress: "..P.."% ".."Current RP: "..N.." RP to next rank "..Q.."")
```


## Emote Calculated RP
```
/run P=(math.floor(GetPVPRankProgress(target)*10000))/100 W=UnitPVPRank("player") N=(W-6)*5000+5000*P/100 Q=(W-5)*5000-N*0.8 SendChatMessage("Rank Progress: "..P.."% ".."Current RP: "..N.." RP to next rank "..Q.."","emote")
```
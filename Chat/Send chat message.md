## Send chat message
```
/run local s,m,c,=SendChatMessage,"<My Message Here>";if UnitInRaid("player")then c="RAID" elseif UnitExists("party1")then c="PARTY" end;s(m,c)
```
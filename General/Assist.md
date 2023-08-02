## Assist / Follow Leader
assist and follow the party leader
```
/run AssistUnit("party"..GetPartyLeaderIndex());FollowUnit("party"..GetPartyLeaderIndex())
```


## Assist / Follow Leader 
assist and follow if a party leader is found
```
/run for i=1,4 do if UnitIsPartyLeader("party"..i) then AssistUnit("party"..i); FollowUnit("party"..i)end end
```


## Non-leaders Assist Name
```
/run if not IsPartyLeader() then AssistByName("Charname") end
```

 
## Non-leaders Assist Party 
```
/run if not IsPartyLeader() then TargetUnit("party1target") end
```


## Assist By Name
```
/run AssistByName("Charname")
```

 
## Assist Party
``` 
/run TargetUnit("party1target")
```

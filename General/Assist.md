## Assist By Name
```
/run AssistByName("Charname")
```

 
## Assist Party
``` 
/run TargetUnit("party1target")
```


## Non-leaders Assist Leader
if your not party leader then assist by name
```
/run if not IsPartyLeader() then AssistByName("Charname") end
```

 
## Non-leaders Assist Party 
```
/run if not IsPartyLeader() then TargetUnit("party1target") end
```

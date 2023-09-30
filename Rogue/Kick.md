## Kick + Say
kicks target and announce your interrupt in say
```
/cast Kick
/run if not TeM then TeM = GetTime() + 10 end if GetTime() > TeM then SendChatMessage("%t Kicked","SAY") TeM = nil end
```


## Kick, and emote you kicking target by name
```
/cast Kick
/e Kicked %t
```
 

## Simple kick macro
```
/cast Kick
/7 %t Kicked
```
With 7 The channel for posting (1 = general, 2 = trade, say, yell, party, raid, etc.)
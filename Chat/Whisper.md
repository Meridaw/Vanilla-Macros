## Whisper hi! to target (doesn't whisper yourself)
```
/run if not UnitIsUnit("player","target") then SendChatMessage("hi!","WHISPER",nil,UnitName("target"))end
```
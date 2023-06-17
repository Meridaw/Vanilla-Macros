## Cast power infusion, send a tell to the target notifying them
```
/cast Power Infusion
/run if UnitExists"target"then SendChatMessage("PI on YOU!! 20% spellpower for 15secs","WHISPER",nil,UnitName"target")end
```


## Power Infusion, yell message if target is friendly and not yourself
```
/cast Power Infusion
/run if not UnitIsUnit("target", "player") and UnitIsFriend ("player", "target") then SendChatMessage("Power Infusion on %t", "YELL")end
```
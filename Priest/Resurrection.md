## Resurrection, message in say and whisper if within range and not casting spell
```
/cast Resurrection
/run local name = UnitName("target"); if CheckInteractDistance("target", 1) and not CastingBarFrame.casting then SendChatMessage("I'm resurrecting you!", "WHISPER", nil, name);SendChatMessage("I'm resurrecting %T!", "SAY")end
```


## Resurrection, message in say and whisper
```
/s I'm resurrecting %T!
/run local name = UnitName("target"); SendChatMessage("I'm resurrecting you!", "WHISPER", nil, name)
/cast resurrection
```
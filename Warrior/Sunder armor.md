## Sunder Armor
shows your target's armor in chat. only if the target armor changes.
```
/cast Sunder Armor
/run a=UnitResistance("target", 0) if a ~= lastArmor then DEFAULT_CHAT_FRAME:AddMessage(a) lastArmor = a end
```


## Sunder on sheep
```
/cast sunder armor
/script ClearTarget();
```
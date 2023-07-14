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


## Combination
uses Sunder Armor, clears target if target is sheeped, shows target's armor
```
/cast Sunder Armor
/run for i=1,16 do if string.find(tostring(UnitDebuff("target",i)),"Polymorph") then ClearTarget() break end end
/run a=UnitResistance("target",0) if a~=lastArmor then SendChatMessage(a,"SAY") lastArmor=a end
```
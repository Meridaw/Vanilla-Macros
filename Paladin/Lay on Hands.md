## Lay on Hands on target if target is a player, else Lay on Hands oneself
```
/run if UnitIsFriend ("player", "target") then CastSpellByName("Lay on Hands") SendChatMessage("Casted Lay on Hands on %t","Emote") else CastSpellByName("Lay on Hands",1)end
```
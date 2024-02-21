## Flash of Light + Trinket
this uses the trinket in inventory slot 13 if you're in combat when it's ready and heals you or a friendly player you target.
```
/run if UnitAffectingCombat("player") and  GetInventoryItemCooldown("player", 13)==0 then UseInventoryItem(13)elseif UnitIsPlayer("target") then CastSpellByName("Flash of Light") else CastSpellByName("Flash of Light",1)  end
```
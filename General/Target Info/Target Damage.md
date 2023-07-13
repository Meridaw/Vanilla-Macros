## Target name and damage
```
/run L, H = UnitDamage("target") DEFAULT_CHAT_FRAME:AddMessage(format("%s Dmg: %.0f - %.0f", GetUnitName("target"), L, H))
```


## Target name, main hand damage and offhand damage
```
/run ld, hd, old, ohd, pb, nb, pm = UnitDamage("target"); SendChatMessage(UnitName("target").."'s main hand attacks hit for "..ld.." to "..hd.. " and their offhand attacks hit for "..old.." to "..ohd);
```
## Target Name and DPS
```
/run L, H = UnitDamage("target"); S = UnitAttackSpeed("target"); DEFAULT_CHAT_FRAME:AddMessage(format("%s DPS: %d", GetUnitName("target"), (L + H)/(2*S)))
```
## Target attack speed in say
```
/run u=UnitAttackSpeed y="target" a=u(y ,0) SendChatMessage(UnitName(y).." has "..a.." seconds per attack. ", SAY)
```
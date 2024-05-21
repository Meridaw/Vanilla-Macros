## Target attack power in say
```
/run u=UnitAttackPower y="target" a=u(y ,0) SendChatMessage(UnitName(y).." has "..a.." Attack Power. ", SAY)
```


## Checking The AP Modifiers
```
/script base, buff, debuff = UnitAttackPower("target"); ap = base + buff + debuff; DEFAULT_CHAT_FRAME:AddMessage(ap.." = "..base.."+"..buff.."+"..debuff);
```


The command for unit attack power returns (base ap), (ap increases), and (ap decreases) for players. <br/>
The command for unit attack power returns (base ap), (ap changes), and (a buggy -1 )for units. <br/>
Mob melee damage is reduced by 0% to 30% based on the percent of how much ap is reduced (if you reduce a mob's ap by 100%, you reduce its damage by 30%). <br/>
Scaling in raids reduces mobs base damage AND base ap (reducing base ap does not reduce the damage directly, but it makes AP debuffs more effective by making them reduce it by a bigger percent). <br/>
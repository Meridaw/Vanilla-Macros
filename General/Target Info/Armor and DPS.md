## Target armor and dps in say
```
/run lowDmg, highDmg=UnitDamage("target") SendChatMessage("%t hits for "..math.ceil((lowDmg+highDmg)/2).." damage every "..tostring(math.floor(UnitAttackSpeed("target")*100)/100).." seconds and has "..UnitResistance("target",0).." Armor.","SAY")
```
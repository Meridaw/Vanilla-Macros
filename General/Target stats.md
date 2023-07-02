## Target armor and resist in chat (only works on self and NPCs)
```
/run local b={"Armor","Holy","Fire","Nature","Frost","Shadow","Arcane"} a=UnitName("target").."'s stats: " for i=0,6 do a = a..b[i+1]..": "..UnitResistance("target", i)..", " end SendChatMessage(a)
```
 

## Target armor and resist in say
```
/run u=UnitResistance y="target" a=u(y ,0) h=u(y ,1) f=u(y ,2) n=u(y ,3) fr=u(y ,4) s=u(y ,5) z=u(y ,6) SendChatMessage(UnitName(y).." has "..a.." Armor, "..h.." HR, "..f.." FR, "..n.." NR, "..fr.." FrR, "..s.." SR and "..z.." AR.", SAY)
```
 

## Target attack power in say
```
/run u=UnitAttackPower y="target" a=u(y ,0) SendChatMessage(UnitName(y).." has "..a.." Attack Power. ", SAY)
```
 

## Target armor and dps in say
```
/run lowDmg, highDmg=UnitDamage("target") SendChatMessage("%t hits for "..math.ceil((lowDmg+highDmg)/2).." damage every "..tostring(math.floor(UnitAttackSpeed("target")*100)/100).." seconds and has "..UnitResistance("target",0).." Armor.","SAY") 
```


## Target name and damage
```
/run L, H = UnitDamage("target") DEFAULT_CHAT_FRAME:AddMessage(format("%s Dmg: %.0f - %.0f", GetUnitName("target"), L, H))
```


## Target attack speed in say
```
/run u=UnitAttackSpeed y="target" a=u(y ,0) SendChatMessage(UnitName(y).." has "..a.." seconds per attack. ", SAY)
```


## Target name, main hand damage and offhand damage
```
/run ld, hd, old, ohd, pb, nb, pm = UnitDamage("target"); SendChatMessage(UnitName("target").."'s main hand attacks hit for "..ld.." to "..hd.. " and their offhand attacks hit for "..old.." to "..ohd);
```


## Target class
```
/run u=UnitClass y="target" a=u(y ,0) SendChatMessage(UnitName(y).." is a "..a..". ", SAY)
```
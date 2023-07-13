## Target armor and resist
Target armor and resist in chat. only works on self and NPCs.
```
/run local b={"Armor","Holy","Fire","Nature","Frost","Shadow","Arcane"} a=UnitName("target").."'s stats: " for i=0,6 do a = a..b[i+1]..": "..UnitResistance("target", i)..", " end SendChatMessage(a)
```
 

## Target armor and resist in say
```
/run u=UnitResistance y="target" a=u(y ,0) h=u(y ,1) f=u(y ,2) n=u(y ,3) fr=u(y ,4) s=u(y ,5) z=u(y ,6) SendChatMessage(UnitName(y).." has "..a.." Armor, "..h.." HR, "..f.." FR, "..n.." NR, "..fr.." FrR, "..s.." SR and "..z.." AR.", SAY)
```
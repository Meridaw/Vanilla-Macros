## Faerie Fire
```
/run a=SendChatMessage z="target" str=UnitName(z) b=UnitExists(z) FF=false for i=1,16 do db=UnitDebuff(z,i) if db and string.find(db,"FaerieFire") then FF=true end end if FF then a("FF true","SAY") elseif b then str=str.." no FF!" a(str,"SAY") end
```
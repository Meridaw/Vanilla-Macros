## Curse of Elements
```
/run a=SendChatMessage z="target" str=UnitName(z) b=UnitExists(z) CoE=false for i=1,16 do db=UnitDebuff(z,i) if db and string.find(db,"ChillTouch") then CoE=true end end if CoE then a("COE true","SAY") elseif b then str=str.." no CoE!" a(str,"SAY") end
```
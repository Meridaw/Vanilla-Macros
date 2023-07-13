## Curse of Shadow
```
/run a=SendChatMessage z="target" str=UnitName(z) b=UnitExists(z) CoS=false for i=1,16 do db=UnitDebuff(z,i) if db and string.find(db,"Achimonde") then CoS=true end end if CoS then a("COS true","SAY") elseif b then str=str.." no CoS!" a(str,"SAY") end
```
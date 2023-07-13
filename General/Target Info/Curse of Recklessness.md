## Curse of Recklessness
```
/run a=SendChatMessage z="target" str=UnitName(z) b=UnitExists(z) CoR=false for i=1,16 do db=UnitDebuff(z,i) if db and string.find(db,"UnholyStrength") then CoR=true end end if CoR then a("COR true","SAY") elseif b then str=str.." no CoR!" a(str,"SAY")end
```
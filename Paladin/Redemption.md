## Redemption, else Holy Light on target / self
```
/run if UnitIsDead("target") then CastSpellByName("Redemption") elseif UnitIsFriend ("player", "target") then CastSpellByName("Holy Light") else CastSpellByName("Holy Light",1)  end
```


## Redemption RP
```
/cast Redemption
/run if not lr or GetTime()-lr>5 then lr=GetTime() if UnitIsDead("target") then i=math.random(1,2) c=i>1 and "%t, you are terminated." or "What, %t has fallen? Arise, my champion!" SendChatMessage(c,"YELL") end end
```
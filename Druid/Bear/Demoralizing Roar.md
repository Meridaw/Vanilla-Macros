## Start attack, Demoralizing Roar (put auto attack on your bars)
```
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z);end;end;end;
/cast Demoralizing Roar
```


## Demoralizing Roar + show target attack power
shows you target attack power after reduction. change 126 depending on roar rank.
```
/cast Demoralizing Roar
/run a=UnitAttackPower("target") - 126 if a ~= lastAttackPower then DEFAULT_CHAT_FRAME:AddMessage(a) lastAttackPower = a end
```
## Simple one-button cleanse
Simple one-button cleanse that prioritizes Curses and saves your GCD
```
/run local d,_,t=UnitDebuff("target",1,1) if d then if t=="Curse" then CastSpellByName("Remove Curse") else CastSpellByName("Abolish Poison") end else DEFAULT_CHAT_FRAME:AddMessage("No dispellable debuff found.") end
```


## Remove Curse
Remove Curse from target if target is a player, else Remove Curse from oneself
```
/run if UnitIsFriend ("player", "target") then CastSpellByName("Remove Curse") else CastSpellByName("Remove Curse",1)  end; TargetLastEnemy();
```
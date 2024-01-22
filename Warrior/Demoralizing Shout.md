## Cast Bloodrage if you have less then 10 rage, else demo shout
```
/script if UnitMana("Player")>=10 then CastSpellByName("Demoralizing Shout"); else CastSpellByName("Bloodrage"); end;
```


## Demoralizing Shout + show target attack power
shows you target attack power after reduction. change 146 depending on shout rank.
```
/cast Demoralizing Shout
/run a=UnitAttackPower("target") - 146 if a ~= lastAttackPower then DEFAULT_CHAT_FRAME:AddMessage(a) lastAttackPower = a end
```
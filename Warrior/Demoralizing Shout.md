Cast Bloodrage if you have less then 10 rage, else demo shout
```
/script if UnitMana("Player")>=10 then CastSpellByName("Demoralizing Shout"); else CastSpellByName("Bloodrage"); end;
```
## Shackle Undead / send chat message
```
/run CastSpellByName("Shackle Undead");
/run if UnitCreatureType("target") == "Undead" then SendChatMessage(">>> Shackling %t, leave it be.","SAY"); end
```


## Shackle Undead and mark it with circle
```
/run CastSpellByName("Shackle Undead");SetRaidTarget("target",2);
```


## Shackle if undead, else Mind Soothe
```
/run if UnitCreatureType("target")=="Undead" then CastSpellByName("Shackle Undead") else CastSpellByName("Mind Soothe")end
```
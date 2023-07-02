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


## Shackle and mark if undead, else Mind Soothe 
It'll mind soothe humanoids, but mark and shackle undead
```
/run if UnitCreatureType("target")=="Undead" then CastSpellByName("Shackle Undead");SetRaidTarget("target",1) else CastSpellByName("Mind Soothe")end
```

Note: You need to adjust the number in SetRaidTarget("target",1) as that number corresponds to a particular marker. iirc, 1 is star, 2 is circle, and so on.
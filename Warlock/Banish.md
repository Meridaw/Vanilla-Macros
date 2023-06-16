## Says what raidmark target you're Banishing 
```
/run i=GetRaidTargetIndex("target");s={"Star","Circle","Diamond","Green","Moon","Square","Cross","Skull"};if UnitName("target") and i then SendChatMessage("Banishing "..s[i],"SAY",nil); end
```


## Banish if demon or elemental, else Fear
```
/run local CT = UnitCreatureType("target") if CT == "Demon" or CT == "Elemental" then CastSpellByName("Banish") else CastSpellByName("Fear") end
```
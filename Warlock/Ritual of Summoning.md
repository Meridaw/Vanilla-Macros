## Ritual of Summoning if friendly target, else Banish
```
/run if UnitIsFriend("player", "target") then SendChatMessage("Summoning %t" ,"emote") CastSpellByName("Ritual of Summoning") else CastSpellByName("Banish")end
```
 

## Summoning macro
```
/script local a = " - 2 people pls click the portal."; local b = UnitName("target"); if (GetNumRaidMembers() > 0) then SendChatMessage("Summoning "..b..a, "RAID"); else SendChatMessage("Summoning "..b..a, "PARTY"); end
/cast Ritual of Summoning
```
 

## Ritual of Summoning, and say who you Summon
```
/say Summoning %t
/cast Ritual of Summoning
```
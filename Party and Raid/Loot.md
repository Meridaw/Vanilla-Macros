## Roll the raidmembers 
Rolls the raidmembers and announce to the chat "Loot goes to X in grp Y !"
```
/run local w = math.random(1,GetNumRaidMembers()) local n, _, g = GetRaidRosterInfo(w) SendChatMessage(format("Loot goes to %s in group %d", n, g),"RAID")
```
 

## Set to common loot (white)
```
/script SetLootMethod("group", 0)
```
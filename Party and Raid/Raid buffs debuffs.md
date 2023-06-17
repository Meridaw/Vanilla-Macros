## Check raid players for specific buff
Combining the above we can do a for loop to check all the players in the raid for a specific debuff. In this example the Brood Affliction: Bronze from the boss Chromaggus in Blackwing Lair. After this boss theres usually a delay of trading Hourglass sand to get rid of the debuff. This macro will list all players in chat who has it.
```
/run b="n_Bronze" n="" r="raid" for i=1,GetNumRaidMembers()do for j=1,40 do if(strfind(tostring(UnitDebuff(r..i,j)),b))then n=UnitName(r..i)..", "..n break end end end if n==""then else SendChatMessage("Players with bronze debuff: "..n,"SAY",nil)end
```
 

## Check raid Bronze debuff from Chromaggus
The following is similar to above but will whisper to each player instead. Depending on server spam protection, this might not work.
```
/run b="n_Bronze" r="raid"for i=1,GetNumRaidMembers()do for j=1,40 do if(strfind(tostring(UnitDebuff(r..i,j)),b))then SendChatMessage("You've got Bronze debuff from Chromaggus use a Hourglass Sand.","WHISPER",nil,UnitName(r..i))break end end end
```

 
## Check raid Fire Protection Potions
The following will instead check for players lacking a certain buff using a tiny function. In this example we’re checking for players who have NOT popped Fire Protection Potions and list them in chat. Remember that this conflicts with the warlock Imp fire resistance buff.
```
/run n=""r="raid"function b(k,l)for i=1,32 do if strfind(tostring(UnitBuff(r..l,i)),k)then return 1 end end end for l=1,GetNumRaidMembers() do if not b("e_FireA",l)then n=UnitName(r..l)..","..n end end SendChatMessage("Pop Fire pot:"..n,"SAY",nil)
```
 

## Whisper each player lacking Fire Protection Potion instead:
```
/run n=""r="raid"function b(k,l)for i=1,32 do if strfind(tostring(UnitBuff(r..l,i)),k)then return 1 end end end for l=1,GetNumRaidMembers() do if not b("e_FireA",l)then SendChatMessage("Pop Fire prot potion!","WHISPER",nil,UnitName(r..l)) end end
```
 

## List players lacking Nature Protection Potion:
```
/run n=""r="raid"function b(k,l)for i=1,32 do if strfind(tostring(UnitBuff(r..l,i)),k)then return 1 end end end for l=1,GetNumRaidMembers() do if not b("e_SpiritA",l)then n=UnitName(r..l)..","..n end end SendChatMessage("Pop Nature pot:"..n,"SAY",nil)
```
 

## Whisper each player lacking Nature Protection Potion:
```
/run n=""r="raid"function b(k,l)for i=1,32 do if strfind(tostring(UnitBuff(r..l,i)),k)then return 1 end end end for l=1,GetNumRaidMembers() do if not b("e_SpiritA",l)then SendChatMessage("Pop Nature prot potion!","WHISPER",nil,UnitName(r..l)) end end
```
 

## List players lacking Shadow Protection Potion:
```
/run n=""r="raid"function b(k,l)for i=1,32 do if strfind(tostring(UnitBuff(r..l,i)),k)then return 1 end end end for l=1,GetNumRaidMembers() do if not b("w_RagingSc",l)then n=UnitName(r..l)..","..n end end SendChatMessage("Pop Shadow pot:"..n,"SAY",nil)
```
 

## Whisper each player lacking Shadow Protection Potion:
```
/run n=""r="raid"function b(k,l)for i=1,32 do if strfind(tostring(UnitBuff(r..l,i)),k)then return 1 end end end for l=1,GetNumRaidMembers() do if not b("w_RagingSc",l)then SendChatMessage("Pop Shadow prot potion!","WHISPER",nil,UnitName(r..l)) end end
```
## Swap 2 players in raid
```
/run local n1,n2,s1,s2="Nicky","Shagu"; for i=1,40 do if UnitName("raid"..i) == n1 then s1 = i elseif UnitName("raid"..i) == n2 then s2 = i end; end; if s1 and s2 then SwapRaidSubgroup(s1, s2) end
```
 

## Go through the whole raid list and demote and kick every player character that is offline.
```
/run for i=1,GetNumRaidMembers() do u="raid"..i n=UnitName(u)if not UnitIsConnected(u) then DemoteAssistant(n)UninviteByName(n)end end
```
 

## Similar to above but will promote every player character.
```
/run for i=1,GetNumRaidMembers() do u="raid"..i n=UnitName(u)if UnitIsConnected(u) then PromoteToAssistant(n)end end
```
 

## Combine both above and promote everyone online but demote and kick everyone that is offline.
```
/run for i=1,GetNumRaidMembers() do u="raid"..i n=UnitName(u)if UnitIsConnected(u) then PromoteToAssistant(n) else DemoteAssistant(n)UninviteByName(n)end end
```
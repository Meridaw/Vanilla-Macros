## Roll Brackets
prints roll brackets for each guild in the raid
```
/run local t={},n,g,r;for i=1,40 do n=GetRaidRosterInfo(i);if n then TargetByName(n);g=tostring(GetGuildInfo("target"));t[g]=t[g] and t[g]+1 or 1;end;end;r=1;for k,v in pairs(t) do SendChatMessage(string.format("%s: %d-%d",k,r,r+v-1),"RAID");r=r+v;end;
```
## Starfire + Moonfire
cast moonfire until nature's grace trigger then cast starfire
```
/run c=CastSpellByName function b(k)for i=1,32 do if strfind(tostring(UnitBuff("player",i)),k)then return 1 end end end if not b("NaturesBlessing")then c("Moonfire(Rank 4)")else c("Starfire")end
```


## Starfire + Wrath
cast wrath until nature's grace trigger then cast starfire
```
/run i=1;m=0;c=CastSpellByName;while(UnitBuff("player",i)~=nil) do if(strfind(UnitBuff("player",i),"Spell_Nature_NaturesBlessing")~=nil) then m=1;end;i=i+1;end;if (m==1) then c"Starfire";else c"Wrath";end;
```
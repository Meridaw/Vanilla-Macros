## Starfire if Nature's Grace, else Wrath
```
/run i=1;m=0;c=CastSpellByName;while(UnitBuff("player",i)~=nil) do if(strfind(UnitBuff("player",i),"Spell_Nature_NaturesBlessing")~=nil) then m=1;end;i=i+1;end;if (m==1) then c"Starfire";else c"Wrath";end;
```
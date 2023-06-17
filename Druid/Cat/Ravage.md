## Ravage if out of combat, Ferocious Bite if 3 combopoint, else Shred
```
/run C=CastSpellByName if not UnitAffectingCombat("player")then C("Ravage") elseif GetComboPoints()>=3 then C("Ferocious Bite") else C("Shred") end UIErrorsFrame:Clear()
```


## Ravage/Shred
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Ability_Ambush" then x=1 end i=i+1 end if x==1 then CastSpellByName("Ravage") else CastSpellByName("Shred")end
```


## Ravage and Shred auto select
```
/script i=1;m=0;while(UnitBuff("player",i)~=nil) do if(strfind(UnitBuff("player",i),"Ability_Ambush")~=nil) then m=1; end;i=i+1;end; c=CastSpellByName; if(m==1) then c("Ravage(rank 4)");else c("Shred(rank 5)");end;
```
## Stopcast, Shield target / self
```
/run SpellStopCasting() if UnitIsPlayer ("target") then CastSpellByName("Power word: Shield") else CastSpellByName("Power word: Shield",1)  end UIErrorsFrame:Hide()
```
 

## Stopcast, Self Shield
```
/script SpellStopCasting()
/script CastSpellByName('Power word: Shield', 1)
```


## Renew/Shield
Will use Major Mana Potion if low on mana, keep renew up and use shield if target gets below 30%hp else cast flash heal.
```
/script if UnitMana("Player") < 380 then use("Major Mana Potion") end;
/script i=1;x=0;m=0;c=CastSpellByName;while(UnitBuff("target",i)~=nil) do if(strfind(UnitBuff("target",i),"Renew")) then m=1;end;i=i+1;end;if(m~=1) then c"Renew";elseif (m==1)and(UnitHealth("target")/UnitHealthMax("target")) < 0.3 then c"Power Word: Shield" c"Flash Heal";else c"Flash Heal(rank 4)";end;
```
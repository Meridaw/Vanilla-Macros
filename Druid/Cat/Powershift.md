## Powershift/shred 
Energy level is set to 30, change to a different number for a different cutoff for when you shift to caster
```
/run u=UnitMana('Player'); c=CastSpellByName; f=UnitPowerType("Player"); if (u<=30) and (f==3) then c"Cat Form"; elseif (f==0) then c"Cat Form"; end; for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z);end;end;end;c"Shred"
```


## Shred, Ferocious Bite, and Powershifting one button option
```
/run if GetComboPoints()>=4 then CastSpellByName("Ferocious Bite") else CastSpellByName("Shred") end
/script u=UnitMana('Player'); c=CastSpellByName; f=UnitPowerType("Player"); if (u<=30) and (f==3) then c"Cat Form"; elseif (f==0) then c"Cat Form"; end;
```
## Pounce if out of combat, Rip if 3 combopoint, else Rake
```
/run C=CastSpellByName if not UnitAffectingCombat("player")then C("Pounce") elseif GetComboPoints()>=3 then C("Rip") else C("Rake") end UIErrorsFrame:Clear()
```


## Pounce/Rake
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Ability_Ambush" then x=1 end i=i+1 end if x==1 then CastSpellByName("Pounce") else CastSpellByName("Rake")end
```
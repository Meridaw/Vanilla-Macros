## Rake/Claw
```
/run local i,x=1,0 while UnitDebuff("target",i) do if UnitDebuff("target",i)=="Interface\\Icons\\Ability_Druid_Disembowel" then x=1 end i=i+1 end if x==0 then CastSpellByName("Rake") else CastSpellByName("Claw")end
```


## Claw/Ferocious Bite 
Change 4 to 5 if you want it to build to 5 combo points before Ferocious Bite
```
/run if GetComboPoints()>=4 then CastSpellByName("Ferocious Bite") else CastSpellByName("Claw") end
```


## Claw/Ferocious Bite with auto targeting + auto attack
```
/run if GetUnitName("target")==nil then TargetNearestEnemy() end if not IsCurrentAction(25) then UseAction(25) end if GetComboPoints()>=5 then CastSpellByName("Ferocious Bite") else CastSpellByName("Claw") end
```
## Wing Clip if melee range, else Concussive Shot
```
/run if CheckInteractDistance("target",3) then CastSpellByName("Wing Clip") else CastSpellByName("Concussive Shot"); end
```
 

## Wing Clip if missing on target
```
/run local i,x=1,0 while UnitDebuff("target",i) do if UnitDebuff("target",i)=="Interface\\Icons\\Ability_Rogue_Trip" then x=1 break end i=i+1 end if x==0 then CastSpellByName("Wing Clip") CastSpellByName("Wing Clip(Rank 1)") end
```
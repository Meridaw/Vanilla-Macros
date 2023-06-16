## Battle Shout, else Heroic Strike
```
/run local z=0 for i=1,27 do t=UnitBuff("player",i) if (t and string.find(t,"BattleShout")) then z=1 break end end if z==1 then CastSpellByName("Heroic Strike") else CastSpellByName("Battle Shout") end
```
 

## Battle shout if not active
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Ability_Warrior_BattleShout" then x=1 end i=i+1 end if x==0 then CastSpellByName("Battle Shout")end
```
## If missing cast Insect Swarm, else cast Moonfire
```
/run local i,x=1,0 while UnitDebuff("target",i) do if UnitDebuff("target",i)=="Interface\\Icons\\Spell_Nature_InsectSwarm" then x=1 end i=i+1 end if x==0 then CastSpellByName("Insect Swarm") else CastSpellByName("Moonfire")end
```
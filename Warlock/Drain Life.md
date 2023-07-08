## Spammable Drain Life
```
/run local i,x=1,0 while UnitDebuff("target",i) do if UnitDebuff("target",i)=="Interface\\Icons\\Spell_Shadow_LifeDrain02" then x=1 end i=i+1 end if x==0 then CastSpellByName("Drain Life")end
```
 

## Spammable Drain Life
```
/script if not CastingBarFrame.channeling then CastSpellByName("Drain Life") end
```
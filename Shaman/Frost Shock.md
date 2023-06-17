## Frost Shock rank 1, max rank if clearcasting
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Shadow_ManaBurn" then x=1 end i=i+1 end if x==1 then CastSpellByName("Frost Shock")else CastSpellByName("Frost Shock(Rank 1)")end
```
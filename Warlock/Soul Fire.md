## Soul Fire/CoE
```
/run local i,x=1,0 while UnitDebuff("target",i) do if UnitDebuff("target",i)=="Interface\\Icons\\Spell_Shadow_ChillTouch" then x=1 end i=i+1 end if x==0 then CastSpellByName("Curse of the Elements") else CastSpellByName("Soul Fire") end
```
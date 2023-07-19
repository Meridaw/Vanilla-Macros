## Seal of Light + Judgement
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Holy_HealingAura" then x=1 end i=i+1 end if x==0 then CastSpellByName("Seal of Light") else CastSpellByName("Judgement")end
```
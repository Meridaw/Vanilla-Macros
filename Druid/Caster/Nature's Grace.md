## If buffed Nature's Grace cast HT4, else cast HT3
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Nature_NaturesBlessing" then x=1 end i=i+1 end if x==0 then CastSpellByName("Healing Touch(Rank 3)") else CastSpellByName("Healing Touch(Rank 4)")end
```
 

## If buffed Nature's Grace cast HT3, else cast Regrowth 4
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\Icons\Spell_Nature_NaturesBlessing" then x=1 end i=i+1 end if x==0 then CastSpellByName("Regrowth(Rank 4)") else CastSpellByName("Healing Touch(Rank 3)")end
```
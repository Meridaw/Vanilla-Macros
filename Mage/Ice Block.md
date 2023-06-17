## StopCasting, then Ice Block
```
/run SpellStopCasting() local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Frost_Frost" then x=1 end i=i+1 end if x==0 then CastSpellByName("Ice Block")end
```
 

## Spammable Ice Block
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Frost_Frost" then x=1 end i=i+1 end if x==0 then CastSpellByName("Ice Block")end
```
 

## Ice Block, else cancel Ice Block
```
/run local i,a,sn sn="Ice Block" i=0 while a~=sn do i=i+1 a=GetSpellName(i,"spell")end if ({GetSpellCooldown(i,"spell")})[3]~=0 == not IsShiftKeyDown() then CastSpellByName(sn)end
```
 

## Cold Snap if Ice Block on cooldown, else Ice Block (put Ice Block in action slot 42)
```
/run enable = GetActionCooldown(42) if enable==0 then CastSpellByName("Ice Block") else CastSpellByName("Cold Snap")end
```
## Earth Shock/Lightning Shield
```
/run CastSpellByName("Earth Shock") local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Nature_LightningShield" then x=1 end i=i+1 end if x==0 then CastSpellByName("Lightning Shield")end
```
 

## Frost Shock/Lightning Shield
```
/run CastSpellByName("Frost Shock") local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Nature_LightningShield" then x=1 end i=i+1 end if x==0 then CastSpellByName("Lightning Shield")end
```
 

## Flame Shock/Lightning Shield
```
/run CastSpellByName("Flame Shock") local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Nature_LightningShield" then x=1 end i=i+1 end if x==0 then CastSpellByName("Lightning Shield")end
```
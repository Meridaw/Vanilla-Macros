## Shadow Word: Pain
Cast Shadow Word: Pain if it's not already on the target
```
/run local i,x=1,0 while UnitDebuff("target",i) do if UnitDebuff("target",i)=="Interface\\Icons\\Spell_Shadow_ShadowWordPain" then x=1 end i=i+1 end if x==0 then CastSpellByName("Shadow Word: Pain")end
```
 

## Shadow Word: Pain, else Mind Blast
```
/run local i,x=1,0 while UnitDebuff("target",i) do if UnitDebuff("target",i)=="Interface\\Icons\\Spell_Shadow_ShadowWordPain" then x=1 end i=i+1 end if x==0 then CastSpellByName("Shadow Word: Pain")else CastSpellByName("Mind Blast")end
```
 

## Shadow Word: Pain, else Power Word: Shield
```
/run local i,x=1,0 while UnitDebuff("target",i) do if UnitDebuff("target",i)=="Interface\\Icons\\Spell_Shadow_ShadowWordPain" then x=1 end i=i+1 end if x==0 then CastSpellByName("Shadow Word: Pain")else CastSpellByName("Power Word: Shield")end 
```


## Cast Shadow Word: Pain if missing, else Mind Blast/Smite
```
/run local i,z=1,0 do t=UnitDebuff("target",i) if (t and strfind(t,"ShadowWordPain")) then z=1 end end if z==1 then CastSpellByName("Mind Blast")CastSpellByName("Smite") else CastSpellByName("Shadow Word: Pain")end
```
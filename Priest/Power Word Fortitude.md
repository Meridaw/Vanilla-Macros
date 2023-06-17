## Self buff Power Word: Fortitude, Divine Spirit, else Inner Fire
```
/run c=CastSpellByName function b(k)for i=1,16 do if strfind(tostring(UnitBuff("player",i)),k)then return 1 end end end if not b("WordFortitude")then c("Power Word: Fortitude",1)elseif not b("DivineSpirit")then c("Divine Spirit",1)else c("Inner Fire")end
```


## Buff target Power Word: Fortitude, Divine Spirit, else Shadow Protection
```
/run c=CastSpellByName function b(k)for i=1,16 do if strfind(tostring(UnitBuff("target",i)),k)then return 1 end end end if not b("Fortitude")then c("Power Word: Fortitude")elseif not b("DivineSpirit")then c("Divine Spirit")else c("Shadow Protection")end
```


## Mouseover Fortitude
```
/run local C if UnitName("target") then C = true end ClearTarget() CastSpellByName("Power Word: Fortitude") SpellTargetUnit("mouseover") if TargetLastTarget() then TargetUnit("playertarget") elseif not C then ClearTarget() end
```
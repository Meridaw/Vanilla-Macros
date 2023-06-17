## Feral Faerie Fire when shapeshifted, Faerie Fire if not
```
/script i=1;m=0;while(UnitBuff("player",i)~=nil) do if(strfind(UnitBuff("player",i),"Form")~=nil) then m=1; end;i=i+1;end; c=CastSpellByName; if(m==1) then c("Faerie Fire (Feral)()");else c("Faerie Fire");end;
```
 

## Faerie Fire on targettarget if friendly target, else Faerie Fire
```
/run if UnitCanAttack("player","target") == 1 then CastSpellByName("Faerie Fire")else TargetUnit("targettarget") CastSpellByName("Faerie Fire") TargetLastTarget() end
```


## Spammable Faerie Fire
```
/run m=0 for i=1,40 do if(strfind(tostring(UnitDebuff("target",i)),"Spell_Nature_FaerieFire"))then m=1 end end if m==0 then CastSpellByName("Faerie Fire(Rank 4)") end
```
 

## Spammable Faerie Fire/Insect Swarm
```
/run c=CastSpellByName function b(k)for i=1,16 do if strfind(tostring(UnitDebuff("target",i)),k)then return 1 end end end if not b("e_FaerieF")then c("Faerie Fire(Rank 4)")elseif not b("e_InsectSw")then c("Insect Swarm(Rank 1)")end
```
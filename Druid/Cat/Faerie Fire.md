## Feral Faerie Fire when shapeshifted, Faerie Fire if not
```
/script i=1;m=0;while(UnitBuff("player",i)~=nil) do if(strfind(UnitBuff("player",i),"Form")~=nil) then m=1; end;i=i+1;end; c=CastSpellByName; if(m==1) then c("Faerie Fire (Feral)()");else c("Faerie Fire");end;
```
 

## Faerie Fire on targettarget if friendly target, else Faerie Fire
```
/run if UnitCanAttack("player","target") == 1 then CastSpellByName("Faerie Fire")else TargetUnit("targettarget") CastSpellByName("Faerie Fire") TargetLastTarget() end
```
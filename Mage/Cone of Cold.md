## Cone of Cold rank1, if Clearcasting, then max rank Cone of Cold
```
/run SpellStopCasting() local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Shadow_ManaBurn" then x=1 end i=i+1 end if x==1 then CastSpellByName("Cone of Cold")else CastSpellByName("Cone of Cold(Rank 1)")end
```
 

## Cast Fire Blast, else cast Cone of Cold if target in range
```
/run CastSpellByName("Fire Blast") if CheckInteractDistance("target", 2) then CastSpellByName("Cone of Cold")end
```
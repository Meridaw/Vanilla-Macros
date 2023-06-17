## Low rank Arcane Explosion, max rank if Clearcasting
```
/run SpellStopCasting() local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Shadow_ManaBurn" then x=1 end i=i+1 end if x==1 then CastSpellByName("Arcane Explosion")else CastSpellByName("Arcane Explosion(Rank 1)")end
```
 

## Low rank arcane explosion, max rank if combat
```
/run if not UnitAffectingCombat("player") then CastSpellByName("Arcane Explosion(Rank 1)") else CastSpellByName("Arcane Explosion") end
```
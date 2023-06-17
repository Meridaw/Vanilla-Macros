## Start attack, Earth Shock, Purge
```
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z);end;end;end;
/cast Earth Shock
/cast Purge
```
 

## Earth Shock, Start attack, target nearest enemy
```
/run if not PlayerFrame.inCombat then AttackTarget() end
/cast Earth Shock
/target NearestEnemy();
```
 

## Earth Shock rank 1, max rank if clearcasting
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Shadow_ManaBurn" then x=1 end i=i+1 end if x==1 then CastSpellByName("Earth Shock")else CastSpellByName("Earth Shock(Rank 1)")end
```
## Frost Shock / Purge
use frost shock if not on cooldown and purge if frost shock is on cooldown
```
/run local s="Frost Shock";local i=nil;for j=1,180 do local n=GetSpellName(j,BOOKTYPE_SPELL);if n and strfind(n,s) then i=j;break;end end if i then if GetSpellCooldown(i,BOOKTYPE_SPELL)<1 then CastSpellByName(s)else CastSpellByName("Purge")end end
```


## Frost Shock rank 1, max rank if clearcasting
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Shadow_ManaBurn" then x=1 end i=i+1 end if x==1 then CastSpellByName("Frost Shock")else CastSpellByName("Frost Shock(Rank 1)")end
```
## Overpower
```
/run local texture,name,isActive,isCastable = GetShapeshiftFormInfo(1); if isActive then CastSpellByName("Overpower"); else CastSpellByName("Battle Stance()"); end;
```
 

## Better Overpower
```
/script texture,name,isActive = GetShapeshiftFormInfo(1); if isActive then CastSpellByName("Overpower"); end
/run local start, duration, enabled = GetSpellCooldown(32, BOOKTYPE_SPELL) if duration - ( GetTime() - start) > 1.5 then CastSpellByName("Battle Stance") else cast("Bloodthirst");end
``` 


## Overpower / Heroic Strike
searches for overpower on the action bar and uses it if usable, if you have over 20 rage then it uses heroic strike.
/run for i=1,120 do local t=GetActionTexture(i) if t and string.find(t,"MeleeDamage") and IsUsableAction(i) and (UnitMana("Player")>=5) then UseAction(i) end if (UnitMana("Player")>=20) then CastSpellByName("Heroic Strike") end end
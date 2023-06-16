## BerserkerRage
```
/run local texture,name,isActive,isCastable = GetShapeshiftFormInfo(3); if isActive then CastSpellByName("Berserker Rage"); else CastSpellByName("Berserker Stance()"); end;
```
 

## This macro will change to berserker stance if youre not in it, use Berserker rage to become immune to fear and then change back to defensive stance as fast as possible if you spam it.
```
/run i=0 g=GetPlayerBuff b="Berserker " f=GetShapeshiftFormInfo c=CastSpellByName t,n,q=f(3)while not(g(i)==-1)do if(strfind(GetPlayerBuffTexture(g(i)),"re_Ance"))then c("Defensive Stance")else if q then c(b.."Rage")else c(b.."Stance")end end i=i+1 end
```
 

## Stancedance if zerker rage is not on cooldown
```
/script local _,_,h = GetShapeshiftFormInfo(3) if GetSpellCooldown(33, SpellBookFrame.bookType) <= 0 then if h then CastSpellByName("Berserker Rage") else CastSpellByName("Berserker Stance") end else CastSpellByName("Defensive Stance") end
```


## Note: because you all got diffrent spellbooks the spell ID is not the same you need. To find out what your Berserker Rage ID numder is, you do it easily by just typing this ingame:
```
/script for id = 1, 180, 1 do local spellName, subSpellName = GetSpellName(id, SpellBookFrame.bookType);if spellName and string.find(spellName, "Berserker Rage", 1, true) then ChatFrame1:AddMessage("ID is "..id, 1.0, 1.0, 0.5); end; end;
``` 
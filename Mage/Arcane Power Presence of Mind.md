## Arcane Power
```
/script i=1;m=0;while(UnitBuff("player",i)~=nil) do if(strfind(UnitBuff("player",i),"Spell_Nature_Lightning")~=nil) then m=1; end;i=i+1;end; c=CastSpellByName; if(m==0) then c("Arcane Power"); end;
```
 

## AP / ZHC/ PoM
```
/run if  GetInventoryItemCooldown("player", 13)==0 then UseInventoryItem(13)else s={"Arcane Power","Presence of Mind","Frostbolt"} if q==nil then q=0 end q=q+1 if q>getn(s) then q=1 end CastSpellByName(s[q]) end
```
 

## Arcane Power spammable
```
/run local i=0 c=0 for i=1,40 do if strfind(tostring(GetPlayerBuffTexture(GetPlayerBuff(i))),"Spell_Nature_Lightning") then c=1 end end if c==0 then CastSpellByName("Arcane Power") end
```
 

## Optional edit with the addition of also casting Frostbolt if the buff is active!
```
/run local i=0 t=0 c=CastSpellByName for i=1,40 do if strfind(tostring(GetPlayerBuffTexture(GetPlayerBuff(i))),"Spell_Nature_Lightning") then t=1 end end if t==0 then c("Arcane Power") else c("Frostbolt(Rank 10)") end
```

## Presence of Mind spammable
```
/run local i=0 t=0 c=CastSpellByName for i=1,40 do if strfind(tostring(GetPlayerBuffTexture(GetPlayerBuff(i))),"Spell_Nature_EnchantArmor") then t=1 end end if t==0 then c("Presence of Mind") else c("Frostbolt(Rank 10)") end
```
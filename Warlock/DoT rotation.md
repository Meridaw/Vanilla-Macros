## Warlock DoT rotation – Apply dots when needed

This macro will apply DoT debuffs when needed. There are the same drawbacks to this as Priest Mind Flay above that it can’t distinguish between your own debuffs and fellow warlocks. Still, its quite useful for grinding or when you’re the lone warlock in group. Another limitation is the length of the macro. In order to fit the 255 character limit the debuff names have to be shortened, this could cause conflicts in case a debuff with a similar name is already applied.

## Example:

Curse of Agony = Spell_Shadow_CurseOfSargeras<br/>
Corruption = Spell_Shadow_AbominationExplosion<br/>
Siphon Life = Spell_Shadow_Requiem<br/>

## Order Alternative a) 1) Corruption, 2) Curse of Agony, 3) Siphon Life
```
/run c=CastSpellByName function b(k)for i=1,16 do if strfind(tostring(UnitDebuff("target",i)),k)then return 1 end end end if not b("ionExp")then c("Corruption(Rank 6)")elseif not b("eOfSar")then c("Curse of Agony(Rank 6)")else c("Siphon Life(Rank 4)")end
```
 
 

## Order alternative b) 1) Siphon Life, 2) Corruption, 3) Curse of agony
```
/run c=CastSpellByName function b(k)for i=1,16 do if strfind(tostring(UnitDebuff("target",i)),k)then return 1 end end end if not b("w_Requ")then c("Siphon Life(Rank 4)")elseif not b("ionExp")then c("Corruption(Rank 6)")else c("Curse of Agony(Rank 6)")end
```
 
 

## Order alternative c) 1) Siphon Life, 2) Curse of agony, 3) Corruption
```
/run c=CastSpellByName function b(k)for i=1,16 do if strfind(tostring(UnitDebuff("target",i)),k)then return 1 end end end if not b("w_Requ")then c("Siphon Life(Rank 4)")elseif not b("eOfSarg")then c("Curse of Agony(Rank 6)")else c("Corruption(Rank 6)")end
```
 

If you dislike all the above theres always the “dumb” rotation. This doesn’t take anything into account, it simply rotates everytime you click. Don’t click faster than the global cooldown and keep in mind your mana.

## Dumb dot rotation
1. Siphon Life(Rank 4)<br/>
2. Curse of Agony(Rank 6)<br/>
3. Corruption(Rank 6)<br/>
4. Immolate(Rank 4)<br/>
```
/run s={"Siphon Life(Rank 4)","Curse of Agony(Rank 6)","Corruption(Rank 6)","Immolate(Rank 4)"} if q==nil then q=0 end q=q+1 if q>getn(s)then q=1 end CastSpellByName(s[q])
```
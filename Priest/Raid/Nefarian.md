## Stop casting if priest class call, else heal
```
/run function b(k)for i=1,32 do if strfind(tostring(UnitDebuff("player",i)),k)then return 1 end end end if not b("Spell_Shadow_DetectInvisibility")then CastSpellByName("Greater Heal(Rank 1)")else SpellStopCasting()end
```
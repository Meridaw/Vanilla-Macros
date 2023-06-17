## Nature's Swiftness/Healing wave
```
/script local x=0;for i=1,90 do if IsCurrentAction(i) then x=1 end end if x==0 then CastSpellByName("Nature's Swiftness");SpellStopCasting();CastSpellByName("Healing wave") end
```
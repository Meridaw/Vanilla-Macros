## Nature's Swiftness/Healing wave
```
/script local x=0;for i=1,90 do if IsCurrentAction(i) then x=1 end end if x==0 then CastSpellByName("Nature's Swiftness");SpellStopCasting();CastSpellByName("Healing Touch") end
```
 

## Nature's Swiftness + Healing Touch - without global cooldown
```
/cast Nature's Swiftness
/script SpellStopCasting();
/cast Healing Touch(Rank 10)
/script if ( SpellIsTargeting() ) then SpellTargetUnit ("player"); end
```
 

## Nature's Swiftness, Wrath/Healing Touch
```
/run CastSpellByName("Nature's Swiftness") if UnitCanAttack("player","target") == 1 then CastSpellByName("Wrath") else CastSpellByName("Healing Touch")end
```


## Nature's Swiftness and Max Healing Touch combo
```
/cast Nature's Swiftness
/cast Healing Touch(Rank 11)
```
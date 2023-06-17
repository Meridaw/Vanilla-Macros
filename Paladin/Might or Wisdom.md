## If Warrior or Rogue cast Blessing of Might, else cast Blessing of Wisdom
```
/run class=UnitClass("target"); if ((class=="Rogue") or (class=="Warrior")) then CastSpellByName("Blessing of Might"); else CastSpellByName("Blessing of Wisdom"); end
```
 

## Blessing of Wisdom if target got mana, else Blessing of Might
```
/run power = UnitPowerType("target"); if ( power == 0 ) then CastSpellByName("Blessing of Wisdom") else CastSpellByName("Blessing of Might") end; if ( SpellIsTargeting() ) then CastSpellByName("Blessing of Might"); TargetUnit("player"); end
```
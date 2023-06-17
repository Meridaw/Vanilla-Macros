## Spammable Blizzard
```
/run if not SpellIsTargeting() and not CastingBarFrame.channeling then CastSpellByName("Blizzard")end
```
 

## Blizzard
```
/run local s=SpellIsTargeting if not (s()) then CastSpellByName("Blizzard") end
```
 

## Cast rank 1 if out of combat, else cast max rank
```
/run if not UnitAffectingCombat("player") then CastSpellByName("Blizzard(Rank 1)") else CastSpellByName("Blizzard") end
```
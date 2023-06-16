## Spammable Hellfire
```
/script if not CastingBarFrame.channeling then CastSpellByName("Hellfire") end
```
 

## Spammable Rain of Fire
```
/run if not SpellIsTargeting() and not CastingBarFrame.channeling then CastSpellByName("Rain of Fire")end
```
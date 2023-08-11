## Cleanse
```
/run i=(GetMouseFocus().unit) if i then CastSpellByName("Cleanse") SpellTargetUnit(i) else CastSpellByName("Cleanse") end
```
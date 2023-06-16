## Target and attack the pets' active target
```
/run AssistUnit('pet') if UnitExists('target') then if CheckInteractDistance('target',3) then CastSpellByName('Attack') else CastSpellByName('Auto Shot') end end
```
## Target/Tame Beast (edit Lupos for next pet name)
```
/run TargetByName("Lupos", exactMatch);
/run if not CastingBarFrame.channeling then CastSpellByName("Tame Beast"); end;
```
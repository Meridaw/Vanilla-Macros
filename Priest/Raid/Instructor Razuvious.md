## Mind Control if not channeling, else target Instructor Razuvious, cast spells and attack
```
/run if not CastingBarFrame.channeling then CastSpellByName("Mind Control") else TargetByName("Instructor Razuvious", exactMatch);end CastPetAction(1);CastPetAction(2);CastPetAction(3);
```
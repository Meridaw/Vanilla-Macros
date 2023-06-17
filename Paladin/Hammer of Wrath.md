## Hammer of Wrath if target have 20% hp, else Judgement
```
/run if UnitHealth("target")/UnitHealthMax("target") < 0.2 then CastSpellByName("Hammer of Wrath")CastSpellByName("Judgement")else CastSpellByName("Judgement")end
```
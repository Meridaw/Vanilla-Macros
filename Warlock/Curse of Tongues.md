## Curse of Tongues if target got mana, else Curse of Weakness
```
/run if (UnitMana("target")>0) then CastSpellByName("Curse of Tongues") else CastSpellByName("Curse of Weakness") end
```
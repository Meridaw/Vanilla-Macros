## Repentance / send chat message 
```
/run CastSpellByName("Repentance") if SpellCanTargetUnit("target") then SendChatMessage('Repentance on %t', 'Say') else SpellStopTargeting() end
```
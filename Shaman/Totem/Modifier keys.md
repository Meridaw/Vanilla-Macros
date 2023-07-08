## Modifier keys
This macro allows for a second totem to be attached to the same key, while ALT is being hold down aswell.
```
/script if (IsAltKeyDown())then CastSpellByName("TOTEM NAME FOR SHIFT+ALT") else CastSpellByName("TOTEM NAME FOR SHIFT") end
```
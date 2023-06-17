## Instant casting / Cancel any active channeling spell

This is really important to know for all casting classes as it helps you when you change your mind when casting something. Add it to your macros where timing is important.
```	
/run SpellStopCasting()
```
To combine it with a macro that casts another spell simply add it to the beginning of the macro:
```	
/run SpellStopCasting() CastSpellByName("Moonfire(Rank 8)")
```
As a Tauren it’s really useful in combination with War Stomp 🙂
```	
/run SpellStopCasting() CastSpellByName("War Stomp")
```

Made by Sandsten
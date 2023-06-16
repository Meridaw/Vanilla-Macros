## Find SpellBookID (replace SpellName in "SpellName")
```
/script for id = 1, 180, 1 do local spellName, subSpellName = GetSpellName(id, SpellBookFrame.bookType);if spellName and string.find(spellName, "SpellName", 1, true) then ChatFrame1:AddMessage("ID is "..id, 1.0, 1.0, 0.5); end; end;
```


## If you want to test you have the right spell type this into the chat window (replace X with the number you want to test)
```
/script DEFAULT_CHAT_FRAME:AddMessage(GetSpellName(X,0)); 
```

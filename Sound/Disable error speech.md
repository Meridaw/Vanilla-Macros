## Disable Error Speech (SetCVar)
```
/run SetCVar("EnableErrorSpeech", 0) UIErrorsFrame:UnregisterEvent"UI_ERROR_MESSAGE" CastSpellByName"SPELLNAME" UIErrorsFrame:RegisterEvent"UI_ERROR_MESSAGE" SetCVar("EnableErrorSpeech", 1)
```


## Disable Error Speech (Console)
```
/console EnableErrorSpeech 0
/run UIErrorsFrame:UnregisterEvent"UI_ERROR_MESSAGE"
/run CastSpellByName"SPELLNAME"
/run UIErrorsFrame:RegisterEvent"UI_ERROR_MESSAGE"
/console EnableErrorSpeech 1
```
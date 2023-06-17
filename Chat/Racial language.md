## Automatically swap racial language to Taur-ahe (tauren language).
```
/run ChatFrameEditBox.language = (ChatFrameEditBox.language == GetLanguageByIndex(1) and GetLanguageByIndex(2) or GetLanguageByIndex(1)) ChatFrame1:AddMessage(" "..ChatFrameEditBox.language)
```
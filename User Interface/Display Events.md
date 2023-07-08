## Display Events
displays the ongoing events in the chat frame
```
/run local f = CreateFrame('FRAME')f:RegisterAllEvents()f:SetScript('OnEvent', function()DEFAULT_CHAT_FRAME:AddMessage(event)end)
```
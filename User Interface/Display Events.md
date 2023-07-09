## Show / hide Events
toggles on and off the ongoing events in the chat frame
```
/run if not f then f = CreateFrame('FRAME') end if f:GetScript('OnEvent') then f:UnregisterAllEvents()f:SetScript('OnEvent', nil) else f:RegisterAllEvents()f:SetScript('OnEvent', function()DEFAULT_CHAT_FRAME:AddMessage(event)end) end
```


## Show Events
displays the ongoing events in the chat frame
```
/run f = CreateFrame('FRAME')f:RegisterAllEvents()f:SetScript('OnEvent', function()DEFAULT_CHAT_FRAME:AddMessage(event)end)
```


## Hide Events
hides the ongoing events in the chat frame
```
/run f:UnregisterAllEvents()f:SetScript('OnEvent', nil)
```


## Hide redundant Events
this hides some of the redundant chat events
```
/run EventUnregister = {"CHAT_MSG_ADDON", "CHAT_MSG_CHANNEL", "CHAT_MSG_CHANNEL_LEAVE", "CHAT_MSG_CHANNEL_JOIN", "CHAT_MSG_GUILD"} for i = 1, getn(EventUnregister) do f:UnregisterEvent(EventUnregister[i])end
```
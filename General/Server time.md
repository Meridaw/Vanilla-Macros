## Local Server time
```
/run hour,min=GetGameTime()
/run DEFAULT_CHAT_FRAME:AddMessage(format("Server time is %s:%s",hour,min));
```
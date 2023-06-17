## Print a string of your current target to chat log
```
/run DEFAULT_CHAT_FRAME:AddMessage("Hello world! my target name is "..GetUnitName("target"))
```
 

## If your current target is a player then send a chat whisper to him/her
```
/run if UnitExists("target") then SendChatMessage("This is a test but insert whatever you are casting here","WHISPER",nil,UnitName("target")) end
```
 

## The following will send your current location into PARTY chat:
```
/run local x,y=GetPlayerMapPosition("player") SendChatMessage("I'm at "..GetZoneText().." - "..GetMinimapZoneText().." - "..math.floor((x*100)+0,5).." "..math.floor((y*100)+0,5),"PARTY")
```
 

## The following will do the same into BATTLEGROUND chat:
```
/run local x,y=GetPlayerMapPosition("player") SendChatMessage("I'm at "..GetZoneText().." - "..GetMinimapZoneText().." - "..math.floor((x*100)+0,5).." "..math.floor((y*100)+0,5),"BATTLEGROUND")
``` 
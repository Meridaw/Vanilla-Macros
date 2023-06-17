## Coordinates
This macro tells you your current coordinates. I keep it around to help mark locations on my map using Cartographer's note system.
```
/run SetMapToCurrentZone() local x,y=GetPlayerMapPosition("player") DEFAULT_CHAT_FRAME:AddMessage(format("%s, %s: %.1f, %.1f",GetZoneText(),GetSubZoneText(),x*100,y*100))
```
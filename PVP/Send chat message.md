## Assault that target
```
/script SendChatMessage("Assault that level " .. UnitLevel("target") .. " " ..UnitName("target") , "say")
/point
```
 

## Random say
```
/script s={"Die!","Take that!","Smack!","etc"}; SendChatMessage(s[math.random(getn(s))], "SAY")
```
 

## Attack notification
```
/run z="target" x,y=GetPlayerMapPosition("player");SendChatMessage(string.format("%s found at %s! Name:%s Level: %s Type:%s (%d, %d)",UnitClassification(z),GetMinimapZoneText(),UnitName(z),UnitLevel(z),UnitClass(z),1+x*100,1+y*100),"CHANNEL",nil,3); 
```


## Target's name, race and class
```
/run local c, r, n = UnitClass("target"), UnitRace("target"), UnitName("target"); SendChatMessage('Focus ['.. n .. ']! ' .. r .. ' ' .. c .. ' !',"YELL","ORCISH");
```
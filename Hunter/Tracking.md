## Flare, else Track Hidden
```
/run c=CastSpellByName t=GetTrackingTexture() if t and strfind(t,"Stealth") then c("Flare") else CastSpellByName("Track Hidden") end
```
 

## Humanoids/Hidden/Undead/Giants
```
/run c=CastSpellByName t=GetTrackingTexture() if t and strfind(t,"Prayer") then c("Track Hidden") elseif t and strfind(t,"Stealth") then c("Track Undead") elseif t and strfind(t,"Dark") then c("Track Giants") else c("Track Humanoids") end
```
 

## Beasts/Dragonkin/Demons/Elementals
```
/run c=CastSpellByName t=GetTrackingTexture() if t and strfind(t,"_Tracking") then c("Track Dragonkin") elseif t and strfind(t,"Dragon") then c("Track Demons") elseif t and strfind(t,"Fel") then c("Track Elementals") else c("Track Beasts") end
```
 

## Use the script to get the current Tracking Texture
```
/run icon= GetTrackingTexture() DEFAULT_CHAT_FRAME:AddMessage(icon)
```
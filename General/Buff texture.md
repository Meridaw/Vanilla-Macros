## Find Buff Texture 
To find "BUFF_TEXTURE" in certain macros use this macro (Target yourself while you have the buff)
```
/script function m(s) DEFAULT_CHAT_FRAME:AddMessage(s); end for i=1,16 do s=UnitBuff("target", i); if(s) then m("B "..i..": "..s); end s=UnitDebuff("target", i); if(s) then m("D "..i..": "..s); end end
```
 

## Print GetShapeshiftFormInfo(1) in say
```
/run local t,n,a=GetShapeshiftFormInfo(1)DEFAULT_CHAT_FRAME:AddMessage(t..","..n..","..(a and "active" or ""))
```
 

## Use the script to get the current Tracking Texture
```
/run icon= GetTrackingTexture() DEFAULT_CHAT_FRAME:AddMessage(icon)
```
Buffs in vanilla use interface names from the icon they have. That means you use the names of the icons to check instead of the actual buff name. Any more advanced checking wont fit inside a single macro. This is fairly confusing so in order to get the icon name you need to figure it out first.

## List all icon names of buffs of your target.
```
/run for i=1,40 do if UnitBuff("target",i) then DEFAULT_CHAT_FRAME:AddMessage(tostring(i.."="..UnitBuff("target",i)),0.4,1,1) end end
```
 

## List all icon names of debuffs of your target.
```
/run for i=1,40 do if UnitDebuff("target",i) then DEFAULT_CHAT_FRAME:AddMessage(tostring(i.."="..UnitDebuff("target",i)),0.4,1,1) end end
```
 

## Check if a target has a certain buff icon name
```
/run for i=1,40 do if(strfind(tostring(UnitBuff("target",i)),"MyBuffName")) then c="Yes" end end if not c="Yes" then c="No" end DEFAULT_CHAT_FRAME:AddMessage(c)
```
 

## Check if a target has a certain debuff icon name
```
/run for i=1,40 do if(strfind(tostring(UnitDebuff("target",i)),"MyBuffName")) then c="Yes" end end if not c="Yes" then c="No" end DEFAULT_CHAT_FRAME:AddMessage(c)
```
 

There is another way to check proper buff names and buff descriptions by exploiting the tooltip information but it’s unwieldy and requires long bouts of code. This is very unsuitable to be used in macros. Here are some examples if you want to try anyway:

 

## List all the buff names of your target:
```
/run g=GameTooltip g:SetOwner(WorldFrame) t=GameTooltipTextLeft1 for i=1,32 do g:SetUnitBuff("target",i) if t:GetText() then DEFAULT_CHAT_FRAME:AddMessage(i.."="..t:GetText(),0.4,1,1) g:ClearLines() end end g:Hide()
```
 

## List all the buff descriptions of your target:
```
/run g=GameTooltip g:SetOwner(WorldFrame) t=GameTooltipTextLeft2 for i=1,32 do g:SetUnitBuff("target",i) if t:GetText() then DEFAULT_CHAT_FRAME:AddMessage(i.."="..t:GetText(),0.4,1,1) g:ClearLines() end end g:Hide()
```
 

## List all player buff names:
```
/run g=GameTooltip g:SetOwner(WorldFrame) t=GameTooltipTextLeft1 for i=1,32 do g:SetPlayerBuff(i) if t:GetText() then DEFAULT_CHAT_FRAME:AddMessage(i.."="..t:GetText(),0.4,1,1) end end
```
 

## List all player buff descriptions:
```
/run g=GameTooltip g:SetOwner(WorldFrame) t=GameTooltipTextLeft2 for i=1,32 do g:SetPlayerBuff(i) if t:GetText() then DEFAULT_CHAT_FRAME:AddMessage(i.."="..t:GetText(),0.4,1,1) end end
```
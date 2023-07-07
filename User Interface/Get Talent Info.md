## Get Talent Info
prints the name and texture name of talents
```
/run for page = 1,3 do for index = 1,25 do local name, icon = GetTalentInfo(page,index) if name and icon then DEFAULT_CHAT_FRAME:AddMessage(name .. ":" .. icon) end end end
```
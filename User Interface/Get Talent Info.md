## Name and texture name
prints the name and texture name of talents
```
/run for page = 1,3 do for index = 1,25 do local name, icon = GetTalentInfo(page,index) if name and icon then DEFAULT_CHAT_FRAME:AddMessage(name .. ":" .. icon) end end end
```


## Talent page, number and name
print all indexes in the talent trees with talent name
```
/run for page = 1,3 do for index = 1,25 do local name = GetTalentInfo(page,index) if name then DEFAULT_CHAT_FRAME:AddMessage(page .. "," .. index ..": ".. name) end end end
```
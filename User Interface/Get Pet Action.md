## Get Pet Action Info
print name and number of pet skills
```
/run for i=1,100 do if GetPetActionInfo(i) then DEFAULT_CHAT_FRAME:AddMessage("Index "..i..": "..GetPetActionInfo(i)) end end
```
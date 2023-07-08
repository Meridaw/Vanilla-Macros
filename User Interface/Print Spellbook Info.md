## Print skills
prints the name and id of all the skills in your spellbook
```
/run local i=1;while true do local spellName,spellRank=GetSpellName(i,BOOKTYPE_SPELL);if not spellName then break;end;DEFAULT_CHAT_FRAME:AddMessage(i..": "..spellName..'('..spellRank..')');i=i+1;end
```


## Equivalent to
```
/run local i=1;while true do local spellName,spellRank=GetSpellName(i,"spell");if not spellName then break;end;DEFAULT_CHAT_FRAME:AddMessage(i..": "..spellName..'('..spellRank..')');i=i+1;end
```


## Show all your spells in spellbook
prints the spellbook
```
/run local name,rank,i; for i=1,200,1 do name,rank=GetSpellName(i,BOOKTYPE_SPELL); if name then DEFAULT_CHAT_FRAME:AddMessage(i .. " = " .. name .. " / " .. rank); end; end
```
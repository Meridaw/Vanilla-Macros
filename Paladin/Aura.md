## Rotate aura
```
/run s={"Retribution Aura", "Concentration Aura", "Devotion Aura"} if not q then q=1 end CastSpellByName(s[q]) q=q+1 if q>table.getn(s) then q=1 end
```


## Rotate resistance aura
```
/run s={"Fire Resistance Aura", "Shadow Resistance Aura", "Frost Resistance Aura"} if not q then q=1 end CastSpellByName(s[q]) q=q+1 if q>table.getn(s) then q=1 end
```
## use revenge if revenge is useable else cast Shield Block (Put Revenge on action slot 48)
```
/script if not IsUsableAction(48) and GetActionCooldown(48)==0 then CastSpellByName("Shield Block") else CastSpellByName("Revenge") end
```
## BattleShout, else Revenge
Use BattleShout if BattleShout is missing. else cast Revenge.
```
/run local z=0 for i=1,27 do t=UnitBuff("player",i) if (t and string.find(t,"BattleShout")) then z=1 break end end if z==1 then CastSpellByName("Revenge") else CastSpellByName("Battle Shout") end UIErrorsFrame:Clear()
```


## Revenge, else Shield Block 
Use revenge if revenge is useable. else cast Shield Block. Put Revenge on action slot 48.
```
/script if not IsUsableAction(48) and GetActionCooldown(48)==0 then CastSpellByName("Shield Block") else CastSpellByName("Revenge") end
```
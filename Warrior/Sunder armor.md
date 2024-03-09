## Sunder Armor
shows your target's armor in chat. only if the target armor changes.
```
/cast Sunder Armor
/run a=UnitResistance("target", 0) if a ~= lastArmor then DEFAULT_CHAT_FRAME:AddMessage(a) lastArmor = a end
```


## Sunder on sheep
```
/cast sunder armor
/script ClearTarget();
```


## Combination
uses Sunder Armor, clears target if target is sheeped, shows target's armor
```
/cast Sunder Armor
/run for i=1,16 do if string.find(tostring(UnitDebuff("target",i)),"Polymorph") then ClearTarget() break end end
/run a=UnitResistance("target",0) if a~=lastArmor then SendChatMessage(a,"SAY") lastArmor=a end
```


## Sunder if there's not 5 sunders
this one casts sunder if there's not 5 sunders
```
/script local b,c,i; for i = 1, 16 do b = UnitDebuff("target", i); if b and strfind(b, "Ability_Warrior_Sunder") then b, c = UnitDebuff("target", i); break; end; end; if not c or c < 5 then CastSpellByName("Sunder Armor") end;
```
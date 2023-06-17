## Arcane Intellect on mouseover target
```
/run pt='mouseover' t='target' p='player' s='Arcane Intellect' if UnitExists(pt) and UnitIsFriend(p, pt) then TargetUnit(pt) CastSpellByName(s) TargetLastTarget() elseif UnitExists(t) then CastSpellByName(s) else CastSpellByName(s) end
```


## Arcane Intellect on mouseover party frames
```
/run s='Arcane Intellect' f=GetMouseFocus():GetName() t="party"..string.gsub(f, "PartyMemberFrame", "") if UnitExists(t) then TargetUnit(t) CastSpellByName(s) TargetLastTarget() else CastSpellByName(s) end
```
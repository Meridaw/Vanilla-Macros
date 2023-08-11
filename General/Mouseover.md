Checks to see if your mouse cursor is hovering over an applicable target (party frames and nameplates work also) and casts the spell on said target if so. If your cursor is not hovering over an applicable target, it just casts the spell normally as it would if you weren't using a macro.

## Mouseover
```
/run local u=UnitExists("mouseover") and "mouseover" or UnitExists("target") and "target" or "player" CastSpellByName("Healing Touch") SpellTargetUnit(u)
```


## GetMouseFocus Mouseover
```
/run i=(GetMouseFocus().unit) if i then CastSpellByName("Healing Touch") SpellTargetUnit(i) end
```


## Offensive abilities (debuffs, CC, interrupts, DoTs, taunts, etc):
```
/run c=CastSpellByName s="SPELLNAME" if UnitExists("mouseover") and UnitReaction("mouseover","player")<5 then TargetUnit("mouseover") c(s) TargetLastTarget() else c(s) end
```
 

## Friendly abilities (heals, cleanse, Rebirth, etc):
```
/run c=CastSpellByName s="SPELLNAME" if UnitExists("mouseover") and UnitReaction("mouseover","player")>4 then TargetUnit("mouseover") c(s) TargetLastTarget() else c(s) end
```
 

## Both (ex: Paladin's Holy Shock - heals friendlies, hurts enemies):
```
/run c=CastSpellByName s="SPELLNAME" if UnitExists("mouseover") then TargetUnit("mouseover") c(s) TargetLastTarget() else c(s) end
```

## Simple mouseover macro
```
/run TargetUnit("mouseover")
/cast spellname
/run TargetLastTarget()
``` 
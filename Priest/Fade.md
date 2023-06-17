## Fade if in group, else Inner Fire
```
/run SpellStopCasting() if GetNumPartyMembers() == 0 then CastSpellByName("Inner Fire") else CastSpellByName("Fade") end
```


## Fade
```
/run UIErrorsFrame:Hide()
/run SpellStopCasting()
/run CastSpellByName("Fade",1)
```
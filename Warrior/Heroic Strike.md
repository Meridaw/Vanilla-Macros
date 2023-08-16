## Start attack, Heroic Strike
```
/cast Heroic Strike
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z);end;end;end;
```

## Toggle Heroic Strike
```
/run if n~= 1 then CastSpellByName("Heroic Strike") n=1 else SpellStopCasting() n=0 end;
```


## Interrupt Heroic Strike
```
/run SpellStopCasting()
```
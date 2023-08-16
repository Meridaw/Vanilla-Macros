## Heroic Strike
starts auto-attack and turns on Heroic Strike.
```
/cast Heroic Strike
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z);end;end;end;
```

## Toggle Heroic Strike
turns on and off heroic strike.
```
/run if n~= 1 then CastSpellByName("Heroic Strike") n=1 else SpellStopCasting() n=0 end;
```


## Toggle Heroic Strike 40 Rage
turns on and off heroic strike. set to only turn on from 40+ rage.
```
/run if n~= 1 and UnitMana("player")>=40 then CastSpellByName("Heroic Strike") n=1 else SpellStopCasting() n=0 end;
```


## Interrupt Heroic Strike
interrupts the expected heroic strike.
```
/run SpellStopCasting()
```
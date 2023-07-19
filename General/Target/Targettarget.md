## Targettarget
target your target's target, then cast the spell
```
/run TargetUnit("targettarget") CastSpellByName("spell")
```


## Targettarget + target last target
target your target's target, then cast the spell, then target the previous target
```
/run TargetUnit("targettarget") CastSpellByName("spell") TargetLastTarget()
```
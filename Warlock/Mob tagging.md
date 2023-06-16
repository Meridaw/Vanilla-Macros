## Named mob tagging
```
/script ClearTarget();
/target Verog
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z);end;end;end;
/cast Shadowburn
```
 

## Tagging closest mob
```
/script ClearTarget();
/run TargetNearestEnemy()
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z);end;end;end;
/cast Shadowburn
```
 

Macro by Lighthammer 
## Spammable fear with stopcasting (# being the id of the action bar where you put Fear)
```
/script if GetUnitName("target")==nil then TargetNearestEnemy() end
/script if not IsCurrentAction(#) then SpellStopCasting() end;
/cast Fear(Rank 3)
```
 

## Fear with stop casting
```
/script SpellStopCasting()
/cast Fear
```
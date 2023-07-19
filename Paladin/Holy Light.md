## Holy Light
```
/run if UnitIsPlayer("target") then CastSpellByName("Holy Light") else CastSpellByName("Holy Light",1)  end; TargetLastEnemy();UIErrorsFrame:Clear()
```


## Heal party member
Heals party member with lowest health and selects last targeted enemy.
```
/script P=1;T='player';function F(a)h=UnitHealth(a);p=h/UnitHealthMax(a);if h>0 and P>p then P=p;T=a;end end F(T);for i=1,4 do p='party'..i;if p then F(p);end end TargetUnit(T);CastSpellByName('Holy Light');TargetLastEnemy()
```
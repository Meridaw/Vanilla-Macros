## Bloodthirst (put auto attack in action slot 24)
```
/run if not IsCurrentAction(24) then UseAction(24) end;
/run CastSpellByName("bloodthirst")
```
 

## Prioritize BT  over execute when AP breaks 2k (change if BTDmg to 820 if you don't use imp exe)
```
/script local a,b,c=UnitAttackPower("player"); local AP=a+b+c; local BTDmg=AP*0.45; if BTDmg>=900 and UnitMana("player")>=30 then CastSpellByName("Bloodthirst") end
/cast execute
```
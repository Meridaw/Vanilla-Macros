## If not enraged /sit else /stand
```
/run local i,x=1,0 while UnitBuff("player",i) do if string.find(UnitBuff("player",i),"Spell_Shadow_UnholyFrenzy")then x=1 end i=i+1 end if x==1 then DoEmote("STAND")end if x==0 then SpellStopCasting() DoEmote("SIT")end
```
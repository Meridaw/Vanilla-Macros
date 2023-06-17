## 1. Dismount macro 
Not very useful by itself, but is used for other macros. I placed it into slot №27, see the action bar slot reference:

ActionBar page 1: slots 1 to 12<br/>
ActionBar page 2: slots 13 to 24<br/>
ActionBar page 3 (Right ActionBar): slots 25 to 36<br/>
ActionBar page 4 (Right ActionBar 2): slots 37 to 48<br/>
ActionBar page 5 (Bottom Right ActionBar): slots 49 to 60<br/>
ActionBar page 6 (Bottom Left ActionBar): slots 61 to 72<br/>

``` 
/run local i=0 g=GetPlayerBuff while not (g(i) == -1) do if(strfind(GetPlayerBuffTexture(g(i)),"Mount"))then CancelPlayerBuff(g(i)) end i=i+1 end
```

## 2. Dismount + switch to caster form - somewhat useful, but still mainly used by other macros. I placed it into slot №37.
```
/run UseAction(27)
/run for i=1, GetNumShapeshiftForms() do _, name, active = GetShapeshiftFormInfo(i) if( active ~= nil ) then CastShapeshiftForm(i) break end end
```

## 3. Cat form.

It will dismount/cancel any other form and then switch to the cat form, and if you're already there, it will activate "Track Humanoids".
```
/script c=CastSpellByName; f=UnitPowerType("Player"); if not (f==3) then UseAction(37); else c"Track Humanoids"; end; if (f==0) then c"Cat Form"; end;
```

## 4. Bear form.
Same as above, but for dire bear form. You have to edit it if you only have normal bear form. 
```
/script c=CastSpellByName; f=UnitPowerType("Player"); if not (f==1) then UseAction(37); else end; if (f==0) then c"Dire Bear Form"; end;
```

## 5. Travel form.

Unlike other macros, it won't cancel any other form, so you have to use it while you're in caster form already.
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Ability_Druid_TravelForm" then x=1 end i=i+1 end if x==0 then CastSpellByName("Travel Form") else end﻿
```
You can place all those macros whenever you want, just make sure that commands like UseAction() link to a correct macro.

 

Made by Oakenlix
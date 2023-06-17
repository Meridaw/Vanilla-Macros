## Use evocation if mana is low, and keeping ice barrier up
```
/run if UnitMana("player")< 500 then CastSpellByName("Evocation")end local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Ice_Lament" then x=1 end i=i+1 end if x==0 then CastSpellByName("Ice Barrier")end
```
 

## Ice Barrier, Mana Shield
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Ice_Lament" then x=1 end i=i+1 end if x==0 then CastSpellByName("Ice Barrier")else CastSpellByName("Mana Shield")end
```
 

## Spammable Evocation
```
/script if not CastingBarFrame.channeling then CastSpellByName("Evocation"); end﻿﻿;
```
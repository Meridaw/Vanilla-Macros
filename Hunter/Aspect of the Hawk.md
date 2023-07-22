## Aspect of the Hawk + Aimed Shot
Aspect of the Hawk if not buffed, else Aimed Shot
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Nature_RavenForm" then x=1 end i=i+1 end if x==0 then CastSpellByName("Aspect of the Hawk") else CastSpellByName("Aimed Shot")end
```
 

## Aspect of the Hawk / Monkey
```
/run if(UnitBuff("player",1)==nil)then CastSpellByName("Aspect of the Hawk")elseif(string.find(UnitBuff("player",1), "Raven"))then CastSpellByName("Aspect of the Monkey")elseif(UnitBuff("player",1))then CastSpellByName("Aspect of the Hawk");end
```
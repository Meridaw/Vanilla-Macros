## Life tap when low on mana, else Shadowbolt.
```
/run if UnitMana("Player") < 500 then CastSpellByName("Life Tap")end
/cast Shadow Bolt
```
 

## Curse of Shadow, else Shadow Bolt
```
/run local i,x=1,0 while UnitDebuff("target",i) do if UnitDebuff("target",i)=="Interface\\Icons\\Spell_Shadow_CurseOfAchimonde" then x=1 end i=i+1 end if x==0 then CastSpellByName("Curse of Shadow") else CastSpellByName("Shadow Bolt")end
```
 

## Curse of the Elements, else Shadow Bolt
```
/run local i,x=1,0 while UnitDebuff("target",i) do if UnitDebuff("target",i)=="Interface\\Icons\\Spell_Shadow_ChillTouch" then x=1 end i=i+1 end if x==0 then CastSpellByName("Curse of the Elements") else CastSpellByName("Shadow Bolt")end
```
 

## Curse of Recklessness, else Shadow Bolt
```
/run local i,x=1,0 while UnitDebuff("target",i) do if UnitDebuff("target",i)=="Interface\\Icons\\Spell_Shadow_UnholyStrength" then x=1 end i=i+1 end if x==0 then CastSpellByName("Curse of Recklessness") else CastSpellByName("Shadow Bolt")end
```
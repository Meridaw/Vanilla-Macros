## Stealth
```
/run if GetBonusBarOffset() == 0 then CastSpellByName("Stealth") end
```


## Stealth
```
/run local _, _, active = GetShapeshiftFormInfo(1) if not active then CastShapeshiftForm(1)end
```


## Stealth
```
/run for i=1,120 do if IsCurrentAction(i) and not IsAttackAction(i) then return end end CastSpellByName("Stealth")
```
 

## Stealth 
uses stealth if it's not active. stealth needs to be in action slot 37.
```
/run if not IsCurrentAction(37) then UseAction(37) end;
```
 

## Stealth, if shift key down cancel stealth
```
/run local i,a,sn sn="Stealth" i=0 while a~=sn do i=i+1 a=GetSpellName(i,"spell")end if ({GetSpellCooldown(i,"spell")})[3]~=0 == not IsShiftKeyDown() then CastSpellByName(sn)end
```
 
 
## Here you can see where the actionID slots in your actionbars are:

ActionBar page 1: slots 1 to 12<br/>
ActionBar page 2: slots 13 to 24<br/>
ActionBar page 3 (Right ActionBar): slots 25 to 36<br/>
ActionBar page 4 (Right ActionBar 2): slots 37 to 48<br/>
ActionBar page 5 (Bottom Right ActionBar): slots 49 to 60<br/>
ActionBar page 6 (Bottom Left ActionBar): slots 61 to 72<br/>
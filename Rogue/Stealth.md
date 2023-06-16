## Spammable stealth, if shift key down cancel stealth
```
/run local i,a,sn sn="Stealth" i=0 while a~=sn do i=i+1 a=GetSpellName(i,"spell")end if ({GetSpellCooldown(i,"spell")})[3]~=0 == not IsShiftKeyDown() then CastSpellByName(sn)end
```
 

## Spammable stealth
```
/run local _, _, active = GetShapeshiftFormInfo(1) if not active then CastShapeshiftForm(1)end
```
 

## Unstealth
```
/run local _, _, active = GetShapeshiftFormInfo(1) if active then CastShapeshiftForm(1)end
```
 

## Stealth + Kidney/Cheap Shot
```
/script if UnitAffectingCombat("player")then CastSpellByName("Kidney Shot")else local _, _, active = GetShapeshiftFormInfo(1) if not active then CastShapeshiftForm(1)end end
/cast Cheap Shot
```
 

## Stealth (Put Stealth in action slot 37)
```
/script if not IsCurrentAction(37) then UseAction(37) end;
```
 

## Unstealth: (Put Stealth in action slot 37)
```
/script if IsCurrentAction(37) then UseAction(37) end;
```
 

## Spam stealth, ambush
```
/run local _, _, active = GetShapeshiftFormInfo(1) if not active then CastShapeshiftForm(1)end
/run CastSpellByName("Ambush")
```


## Spam stealth, cheap shot
```
/run local _, _, active = GetShapeshiftFormInfo(1) if not active then CastShapeshiftForm(1)end
/run CastSpellByName("Cheap Shot")
```


## Spam stealth, garrote
```
/run local _, _, active = GetShapeshiftFormInfo(1) if not active then CastShapeshiftForm(1)end
/run CastSpellByName("Garrote")
```


## Spam stealth, sap
```
/run local _, _, active = GetShapeshiftFormInfo(1) if not active then CastShapeshiftForm(1)end
/run CastSpellByName("Sap")
```


## Auto attack, hemo
```
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z);end;end;end;
/run CastSpellByName("Hemorrhage")
```
 
## Here you can see where the actionID slots in your actionbars are:

ActionBar page 1: slots 1 to 12<br/>
ActionBar page 2: slots 13 to 24<br/>
ActionBar page 3 (Right ActionBar): slots 25 to 36<br/>
ActionBar page 4 (Right ActionBar 2): slots 37 to 48<br/>
ActionBar page 5 (Bottom Right ActionBar): slots 49 to 60<br/>
ActionBar page 6 (Bottom Left ActionBar): slots 61 to 72<br/>
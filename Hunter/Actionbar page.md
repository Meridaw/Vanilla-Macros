## Aspect actionbar change
```
/cast Aspect of the Hawk
/script CURRENT_ACTIONBAR_PAGE = Y;
/script ChangeActionBarPage();
/script UIErrorsFrame:Clear()
```
Set number of action bar u wanna switch to insted of Y letter.

 

## Swap to bar 2 if you got a target in melee range, else use Auto Shot (Put Auto Shot in action slot 48)
```
/run if CheckInteractDistance("target",3) then CURRENT_ACTIONBAR_PAGE = 2; ChangeActionBarPage(); else if not IsAutoRepeatAction(48) then CastSpellByName("Auto Shot"); end end
```
 

## Swap to bar 2 if you got a target in melee range, else cast Concussive Shot
```
/run if CheckInteractDistance("target",3) then CURRENT_ACTIONBAR_PAGE = 2; ChangeActionBarPage(); end
/cast Concussive Shot
```
 

## Swap to bar 1 if you don't have a target in melee range, else cast Raptor Strike and Mongoose Bite
```
/run if not CheckInteractDistance("target",3) then CURRENT_ACTIONBAR_PAGE = 1; ChangeActionBarPage(); else if (not PlayerFrame.inCombat) then AttackTarget() end end
/cast Raptor Strike
/cast Mongoose Bite
```
 

## Swap to bar 1 if you don't have a melee target, else cast Wing clip
```
/run if not CheckInteractDistance("target",3) then CURRENT_ACTIONBAR_PAGE = 1; ChangeActionBarPage(); end
/cast Wing clip
```
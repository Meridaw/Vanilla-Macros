## Berserker Rage:
```
/script texture,name,isActive,isCastable = GetShapeshiftFormInfo(3); if isActive then CastSpellByName("Berserker Rage"); else CastSpellByName("Berserker Stance"); end;
```
What this macro does, is that it change your current stance to Berserker Stance regardless of which stance you are and it will cast Berserker Rage. (Note: You have to press it twice)

 

## Charge:
```
/script texture,name,isActive,isCastable = GetShapeshiftFormInfo(1); if isActive then CastSpellByName("Charge(Rank 3)"); else CastSpellByName("Battle Stance"); end;
/script if not IsCurrentAction(36) then UseAction(36) end;
```
This macro will swap your stance to Battle Stance regardless of which stance you are in and it will cast Charge if the charge ability conditions are met. (Note: You have to press it twice)
Also the last line will make you start attacking instantly while you are charging.

 

## Disarm:
```
/script texture,name,isActive,isCastable = GetShapeshiftFormInfo(2); if isActive then CastSpellByName("Disarm"); else CastSpellByName("Defensive Stance"); end;
```
This will change your stance to Defensive Stance, regardless of which stance you are in and it will attempt to cast Disarm if the disarm ability conditions are met. (Note: You have to press it twice)

 

## Overpower:
```
/script texture,name,isActive,isCastable = GetShapeshiftFormInfo(1); if isActive then CastSpellByName("Overpower(Rank 4)"); else CastSpellByName("Battle Stance"); end;
```
This will change your stance to Battle Stance regardless of which stance you are in and it will attempt to cast Overpower if the overpower ability conditions are met. (Note: You have to press it twice)

 

## Pummel:
```
/script texture,name,isActive,isCastable = GetShapeshiftFormInfo(3); if isActive then CastSpellByName("Pummel(Rank 2)"); else CastSpellByName("Berserker Stance"); end;
```
This will change your stance to Berserker Stance regardless of which stance you are in and it will attempt to cast Pummel if the pummel ability conditions are met. (Note: You have to press it twice)

 

## Recklessness:
```
/script texture,name,isActive,isCastable = GetShapeshiftFormInfo(3); if isActive then CastSpellByName("Recklessness"); else CastSpellByName("Berserker Stance"); end;
```
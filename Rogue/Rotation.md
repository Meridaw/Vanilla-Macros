## A simple Rotation
```
/run SnD=false for i=1,16,1 do db=UnitBuff("player",i) if(db~=nil and string.find(db,"SliceDice")) then SnD=true end end
/run if GetComboPoints("target")==5 then CastSpellByName("Eviscerate()");elseif SnD then CastSpellByName("Sinister Strike()");elseif GetComboPoints("target")==0 then CastSpellByName("Sinister Strike()"); else CastSpellByName("Slice and Dice()"); end
```
it Checks if Slice and Dice is up, if not he casts slice and dice.
if the Target has 5 combo points and SnD is up, he uses eviscerate
only pressing one button, a simple beginning, but more is following !

This Rotation is meant for Pve Sword Rogues who got improved SnD
you als no need SuperMacro because it exceeds the 255 char limit


## Improved Rotation
```
/run RuP=false for r=1,16,1 do db=UnitDebuff("target",r) if(db~=nil and string.find(db,"Rupture")) then RuP=true end end
/run SnD=false for i=1,16,1 do db=UnitBuff("player",i) if(db~=nil and string.find(db,"SliceDice")) then SnD=true end end
/run if GetComboPoints("target")==5 then CastSpellByName("Eviscerate()"); end
/run if GetComboPoints("target")==0 then CastSpellByName("Sinister Strike()"); end
/run if SnD then CastSpellByName("Sinister Strike()"); else CastSpellByName("Slice and Dice()"); end
/run if RuP then CastSpellByName("Sinister Strike()"); else CastSpellByName("Rupture()"); end
```
Almost the same as above, but in this case it Checks if you have SnD up, if you dont he recasts it, but also checks if you have Rupture on the Enemy if not he recasts it if he has the Combopoints for it. if Rupture and SnD are up and you reach 5 Cp he does Eviscerate.

This Rotation is meant for Pve Sword Rogues who got improved SnD
you als no need SuperMacro because it exceeds the 255 char limit

If you actually combine this macro with "IsUsableSpell" and insert a spellreaction like Bladefury or Adrenaline Rush, you would have a complete rotation where you dont have to watch for CD's or keeping up your at all. just concentrate on movement and do the best of dps while u move, BUT this is just a theory! (alot of things would still be missing like Autoattack for switching targets and a macro if the current target is not a Boss to use something else, in order to do also MAX dps @trash)


## Ambush, Coldblood & eviscerate
```
/run Stl=false for i=1,16 do db=UnitBuff("player",i) if(db~=nil and string.find(db,"Stealth")) then Stl=true end end
/script if Stl then CastSpellByName("Ambush()"); elseif not Stl then CastSpellByName("Cold Blood()"); elseif GetComboPoints("target")<0 then CastSpellByName("Eviscerate()"); end
```
After using Ambush, instant pop Cold Blood and do eviscerate. Normaly i would like to add Trinkets like the AQ40 trashmob trinket or Ramsteins L Bolt trinket in order to make a oneshot macro, but since i dont have these items, it wont happen :3

-- Request from Confined :3 --


## Rotation to keep every debuff on the Enemy up
```
/run SnD=false for i=1,32,1 do db=UnitBuff("player",i) if(db~=nil and string.find(db,"SliceDice")) then SnD=true end end
/run RuP=false for r=1,16,1 do ddb1=UnitDebuff("target",r) if(ddb1~=nil and string.find(ddb1,"Rupture")) then RuP=true end end
/run ExP=False for e=1,16,1 do ddb2=UnitDebuff("target",e) if(ddb2~=nil and string.find(ddb2,"Warrior_Riposte")) then ExP=true end end
/script AttackTarget();
/run if GetComboPoints("target")==0 then CastSpellByName("Sinister Strike()"); end
/run if SnD then CastSpellByName("Sinister Strike()"); else CastSpellByName("Slice and Dice()"); end
/run if ExP then CastSpellByName("Sinister Strike()"); else CastSpellByName("Expose Armor()"); end
/run if RuP then CastSpellByName("Sinister Strike()"); else CastSpellByName("Rupture()"); end
```
This Rotation is only desired to keep every debuff on the Enemy up, aswell SnD on yourself, the Priority is : "SnD > Expose Armor > Rupture" as Finisher.
Kinda Interessting Idea.

-- Request from LoGyMW --
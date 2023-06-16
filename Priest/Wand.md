Shoot (wand)

/run if not CastingBarFrame.casting then CastSpellByName("Shoot")end UIErrorsFrame:Hide()



Prevent toggling of wand/autoattack

/run GGUseAction=GGUseAction or UseAction;UseAction=function(id,a,b)if not IsCurrentAction(id)and not IsAutoRepeatAction(id)then GGUseAction(id,a,b)end end
/cast Shoot

 

Cast Inner Fire, else spammable Wand "Shoot" (Put Shoot in action slot 37)

/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Holy_InnerFire" then x=1 end i=i+1 end if x==0 then CastSpellByName("Inner Fire") else UseAction(37) end

 

Target/Mashable Wand (Put Shoot in action slot 12)

/script UIErrorsFrame:Hide()
/script if (UnitName('target')==nil) then TargetNearestEnemy() else if not IsAutoRepeatAction(12) then CastSpellByName("Shoot") end;end 



Spammable auto Attack/Shoot (put "Shoot" into action slot 1, and also "Attack" into any action slot)

/run if CheckInteractDistance("target", 3) and (not PlayerFrame.inCombat) then AttackTarget() elseif not IsAutoRepeatAction(6) then CastSpellByName("Shoot") end
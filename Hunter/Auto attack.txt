Spammable Auto Attack Macro w/ Melee and Ranged swapping (put Shoot or Auto Shot into action slot 1)

/run if CheckInteractDistance("target", 3) and (not PlayerFrame.inCombat) then AttackTarget() elseif not IsAutoRepeatAction(1) then CastSpellByName("Auto Shot OR Shoot") end

Replace Auto Shot or Shoot with your classes ranged auto attack

 

Start Melee Attack

/script if (not PlayerFrame.inCombat) then AttackTarget() end

 

Auto Shot

/script if not IsAutoRepeatAction(xx) then CastSpellByName("Auto Shot"); end

 

Auto attack

/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z);end;end;end;
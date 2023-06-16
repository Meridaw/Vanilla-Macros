TargetNearestEnemy, Auto Shot/Attack, Hunter's Mark (put Auto Shot in slot 48)

/run if GetUnitName("target")==nil then TargetNearestEnemy()end;if CheckInteractDistance("target", 3) and (not PlayerFrame.inCombat) then AttackTarget() elseif not IsAutoRepeatAction(48)then CastSpellByName("Auto Shot")end;CastSpellByName("Hunter's Mark")



Hunter's Mark if missing

/run local i,x=1,0 while UnitDebuff("target",i) do if UnitDebuff("target",i)=="Interface\\Icons\\Ability_Hunter_SniperShot" then x=1 end i=i+1 end if x==0 then CastSpellByName("Hunter's Mark")end

 

Hunter's Mark/Pet Attack

/run local i,x=1,0 while UnitDebuff("target",i) do if UnitDebuff("target",i)=="Interface\\Icons\\Ability_Hunter_SniperShot" then x=1 end i=i+1 end if x==0 then CastSpellByName("Hunter's Mark") else PetAttack()end

 

Hunter's Mark/Aimed Shot

/run local i,x=1,0 while UnitDebuff("target",i) do if UnitDebuff("target",i)=="Interface\\Icons\\Ability_Hunter_SniperShot" then x=1 end i=i+1 end if x==0 then CastSpellByName("Hunter's Mark") else CastSpellByName("Aimed Shot")end
Arcane Shot/Auto

/run if not GetUnitName("target")then TargetNearestEnemy()end
/cast Arcane Shot(rank 1)
/run if CheckInteractDistance("target", 3)and not PlayerFrame.inCombat then AttackTarget()elseif not IsAutoRepeatAction(3)then CastSpellByName("Auto Shot")end
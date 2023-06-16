Remove Curse from target if target is a player, else Remove Curse from oneself

/run if UnitIsFriend ("player", "target") then CastSpellByName("Remove Curse") else CastSpellByName("Remove Curse",1)  end; TargetLastEnemy();
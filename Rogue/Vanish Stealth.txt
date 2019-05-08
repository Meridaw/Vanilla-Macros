Vanish/Stealth

/script if UnitAffectingCombat("player") then CastSpellByName("Vanish") else CastSpellByName("Stealth") end

 

Vanish/Spammable stealth

/run if UnitAffectingCombat("player") then CastSpellByName("Vanish")end local _, _, active = GetShapeshiftFormInfo(1) if not active then CastShapeshiftForm(1)end
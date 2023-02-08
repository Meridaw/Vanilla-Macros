Craft Linen Bandage (Edit First Aid and Linen Bandage if you need to craft something else)

/run CastSpellByName("First Aid") for r=1,GetNumTradeSkills() do if GetTradeSkillInfo(r) == "Linen Bandage" then DoTradeSkill(r,1) break end end CloseTradeSkill()
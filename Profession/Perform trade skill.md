## Craft Linen Bandage 
Edit First Aid and Linen Bandage if you need to craft something else
```
/run CastSpellByName("First Aid") for r=1,GetNumTradeSkills() do if GetTradeSkillInfo(r) == "Linen Bandage" then DoTradeSkill(r,1) break end end CloseTradeSkill()
```


## Enchant
this perform the enchant or puts the enchant on your cursor. edit in name of enchant and don't remove the quotation marks.
```
/run local ench="Full name of enchant here" for i=1,GetNumCrafts() do if GetCraftInfo(i)==ench then DoCraft(i) return end end
```
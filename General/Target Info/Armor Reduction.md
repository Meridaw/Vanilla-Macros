## Base Reduction
Target base armor and damage reduction
```
/run a=UnitResistance("target" , 0) pl=UnitLevel("player") br=(a/(a+400+85*pl)*100) DEFAULT_CHAT_FRAME:AddMessage(string.format("Target Base Armor = ".. a)) DEFAULT_CHAT_FRAME:AddMessage("Target Base Damage Reduction = ".. br .."%")
```


## Damage Reduction
Target damage reduction after 5 sunders
```
/run a=UnitResistance("target",0) pl=UnitLevel("player") br=(a/(a+400+85*pl)*100) sund=((a-2000)/(a+400+85*pl)*100) tot=(br-sund) DEFAULT_CHAT_FRAME:AddMessage("After 5 Sunders = "..sund.."%") DEFAULT_CHAT_FRAME:AddMessage("Total Reduction = "..tot.."%")
```
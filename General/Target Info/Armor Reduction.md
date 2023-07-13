## Base Reduction
Target base armor and damage reduction
```
/run a=UnitResistance("target" , 0) pl=UnitLevel("player") br=(a/(a+400+85*pl)*100) print(string.format("Target Base Armor = ".. a)) print("Target Base Damage Reduction = ".. br .."%")
```


## Damage Reduction
Target damage reduction after 5 sunders
```
/run a=UnitResistance("target" , 0) pl=UnitLevel("player") br=(a/(a+400+85*pl)*100) sund=((a-2000)/(a+400+85*pl)*100) tot=(br-sund) print("Target Damage Reduction After 5 Sunders = ".. sund .."%") print("Total Reduction = ".. tot .."%")
```
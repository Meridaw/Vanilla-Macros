## Shoot Gun/Bow/Crossbow macro

This macro will combine the abilities Shoot Bow, Shoot Crossbow and Shoot Gun into one button to get rid of the annoyance that Warriors and Rogues are having in vanilla.

## Copy and paste the following into a macro:
```	
/run s="Shoot "r="Crossbow"c=CastSpellByName _,_,i= string.find(GetInventoryItemLink("player",18),"item:(%d+).+%[(.+)%]")_,_,_,_,_,w=GetItemInfo(i)if w==r.."s"then c(s..r)elseif w=="Bows"then c(s.."Bow")else c(s.."Gun")end --CastSpellByName("Shoot Gun")
```

## More info:

You still need to equip ammo.
It wont handle thrown weapons because nobody uses that :>
This might not work if you’re using and addon called Supermacro.
To get the “in range” color change if you’re using the Addon Bongos or Bartender you need to keep –CastSpellByName(“Shoot Gun”) inside the macro. It doesn’t have any effect on the actual macro. It just “tricks” the addon that it’s a regular spell macro.

If you don’t know what the in range thing is it’s when text of an ability becomes red when you’re out of range of your target.
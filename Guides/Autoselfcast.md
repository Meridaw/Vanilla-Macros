## Auto Self Cast with the interface option disabled

Some addons are essential but also annoying. One especially that you can have a heard time healing without is Clique. It’s amazing to use and enables you to bind spells directly when mouse clicking players in your raid interface. The drawback is that in order for it to work you have to disable Auto Self Cast in interface options:

autoselfcastdisabled

autoselfcastwith disabled

It can quickly get annoying to have to toggle this option on and off everytime you’re going to heal. This is possible to “workaround” using macros. Unfortunately you have to make a macro for each spell. In the following examples I will be using Healing Touch, Regrowth and Rejuvenation but you can replace them with whichever spell you wish to cast.


## HealtouchHealing Touch auto self cast macro :
```	
/run s="Healing Touch(Rank 10)" c=CastSpellByName() if (UnitIsFriend("player", "target") ) then c(s) else c(s, 1) end
```


## Regrowth Regrowth auto self cast macro :
```	
/run s="Regrowth(Rank 8)" c=CastSpellByName() if (UnitIsFriend("player", "target") ) then c(s) else c(s, 1) end
```


## RejuveRejuvenation auto self cast macro :
	
/run s="Rejuvenation(Rank 10)" c=CastSpellByName() if (UnitIsFriend("player", "target") ) then c(s) else c(s, 1) end


## Showing spell tooltips

If you want the addon MacroTooltips by Anaron to work you can’t use the above as it wont recognize the compact syntax s=”myspell”. You have to use the full spell name inside CastSpellByHealing(“MySpell”) instead as in the following macro examples:


## Healing Touch auto self cast macro :
```	
/setspelltooltip Healing Touch
/run if (UnitIsFriend("player", "target")) then CastSpellByName("Healing Touch(Rank 10)") else CastSpellByName("Healing Touch(Rank 10)", 1) end
```


## Regrowth auto self cast macro :
```	
/setspelltooltip Regrowth
/run if (UnitIsFriend("player", "target")) then CastSpellByName("Regrowth(Rank 9)") else CastSpellByName("Healing Touch(Rank 9)", 1) end
```


## Rejuvenation auto self cast macro :
```	
/setspelltooltip Rejuvenation
/run if (UnitIsFriend("player", "target")) then CastSpellByName("Rejuvenation(Rank 10)") else CastSpellByName("Rejuvenation(Rank 10)", 1) end
```


## Cancel form + auto self cast

If you want to combine the above spells with cancel shapeshifting add /script UseAction(37) to the macros.

## Rejuvenation auto self cast + Cancel shapeshift macro :
```	
/setspelltooltip Rejuvenation
/run UseAction(37)
/run if (UnitIsFriend("player", "target")) then CastSpellByName("Rejuvenation(Rank 10)") else CastSpellByName("Rejuvenation(Rank 10)", 1) end
```

Made by Sandsten
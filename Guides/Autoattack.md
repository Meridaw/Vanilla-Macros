## Auto Target + Auto Attack + Cast Spell – combination macro guide

In vanilla when you use your “Attack” ability or press the keybinding for attacking (default: T) this is toggled on/off. Spamming T is really bad if you want to maximize hits. In most situations you don’t want to stop auto attacking, you just want to start!

Here is a step by step walkthrough with explanation of how to write this into any other ability/spell or macro. It is important to understand the different sections in order to adapt this to your preference. You can’t just copy and paste.

Please keep note that in order for the following to work you must make a macro that replaces your spell. You can only do this from inside a macro.

When done editing the macro it should look like the image above. The semicolon “;” separators are not necessary, they are only visual aids.

## 1. Auto targeting part

The following part of the script will check if you currently have no target (nil). If this is the case then target nearest enemy. You can copy and paste this script directly into chat to test it.
```	
/run if GetUnitName("target")==nil then TargetNearestEnemy() end
```

## 2. Auto attacking part

The next part of the script will attempt to use action in action slot 25 if it is not currently active. This is how we enable auto attacking without accidentally stopping the auto attack.
```	
/run if not IsCurrentAction(25) then UseAction(25) end
```
Optional: Hiding the autoattack on macro

If you want you can replace slotID 25 with 13 which is located in the second page of the hidden action bar and place the macro there instead!

## 3. Dragging attack into the action bar

All action bars have a unique slotID. In this example we will use actionbar slot 25. You can change this later if you want.
Click and drag the Attack ability from your spell book into slot 25. (Se below)

ActionBar page 1: slots 1 to 12 <br/>
ActionBar page 2: slots 13 to 24 <br/>
ActionBar page 3 (Right ActionBar): slots 25 to 36 <br/>
ActionBar page 4 (Right ActionBar 2): slots 37 to 48 <br/>
ActionBar page 5 (Bottom Right ActionBar): slots 49 to 60 <br/>
ActionBar page 6 (Bottom Left ActionBar): slots 61 to 72

attack actionbarslots

## 4. Casting a spell from a macro

This is quite easy. In order to properly cast a spell in your macro you should not use /cast as this will call a different function. In order to use it in combination with other scripts you should use this function instead:
```	
/run CastSpellByName("Moonfire(Rank 10)")
```

## Please note the following, this is important:

Functions are CaSeSeNsItIvE! You can’t mix lowercase with UPPERCASE letters.
Don’t have any space between the name of the spell and the rank of the spell Moonfire_(Rank 8) will not work but Moonfire(Rank 8) will.
You need to manually edit the rank to cast. If your level is lower than 60 you will have to manually edit the macro to your desired rank.
For abilities that overwrite lower ranks like Heroic Strike(Rank 8) ranks will not work in a macro but Heroic Strike without the parenthesis and rank will.

Optional: If you want to show spell cooldowns and tooltips over macros you need an addon to do this in vanilla. #showtooltip does not work. Either use a custom UI action bar addon like Bongos, Bartender or Anarons MacroTooltip for vanilla. If you use the addon MacroTooltip add /setspelltooltip Moonfire or more compacted /sstt Moonfire to show tooltip and cooldown.

## 5. Combining the different features into the final macro

moonfireMoonfire auto target + auto attack macro:
```	
/run if GetUnitName("target")==nil then TargetNearestEnemy() end if not IsCurrentAction(25) then UseAction(25) end CastSpellByName("Moonfire(Rank 8)")
```

Made by Sandsten
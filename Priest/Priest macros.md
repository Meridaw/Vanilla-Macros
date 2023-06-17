## Priest macros (Thu Oct 19, 2006)

## Auto Bandage

This macro will allow you to use a bandage on yourself without losing your current target.

X = Bag number (0 to 4, right to left)<br/>
Y = Slot number (1 to n, top left to right, where 'n' is the number of slots your bag has)<br/>
```
/script if (not GetContainerItemLink(X,Y)) then OpenBag(X); else UseContainerItem(X,Y); SpellTargetUnit("player"); end
```


## Power Infusion + Inner Focus
For disc/holy priests that want to use PI and IF together with one click
interesting in conjunction with PH as a grp life saver e.g.
```
/target [INSERT NAME HERE]
/script CastSpellByName('Power Infusion');
/script SpellStopCasting();
/script TargetLastTarget();
/script CastSpellByName('Inner Focus');
/script SpellStopCasting();
```

These are stolen from the 'lock forums. ❤️ Graguk from Proudmoore.

## Trinkets:
```
/script if GetInventoryItemCooldown("player", 13) == 0 then UseInventoryItem(13); SpellStopCasting(); end
/script if GetInventoryItemCooldown("player", 14) == 0 then UseInventoryItem(14); SpellStopCasting(); end
```

## Top Trinket + PI
```
/script if GetInventoryItemCooldown("player", 13) == 0 then UseInventoryItem(13); SpellStopCasting(); end
/target [your toon's name]
/cast Power Infusion
/script TargetLastTarget();
```

## Scan Spellbook (used below):
YOU MUST REPLACE FEL DOMINATION WITH THE NAME OF THE COOLDOWN SKILL YOU ARE LOOKING FOR.
```
/script for id = 1, 180, 1 do local spellName, subSpellName = GetSpellName(id, SpellBookFrame.bookType);if spellName and string.find(spellName, "Fel Domination", 1, true) then ChatFrame1:AddMessage("ID is "..id, 1.0, 1.0, 0.5); end; end;
```


## Cooldown skill + spell:
REPLACE 16 WITH THE NUMBER OUTPUT BY THE SCAN MACRO. REPLACE AMPLIFY CURSE WITH THE COOLDOWN SKILL. REPLACE CURSE OF AGONY WITH THE SPELL YOU WANT TO CAST.
```
/script local e, f, g = GetSpellCooldown(16, SpellBookFrame.bookType); if (f <= 0) then CastSpellByName("Amplify Curse"); SpellStopCasting();end; CastSpellByName("Curse of Agony");
```


## PI Whisper Notification to Target
```
/cast Power Infusion
/script local n=UnitName("target");SendChatMessage("You have been infused.","WHISPER","COMMON",n);
```

## Self cast without loosong target

These macro's will self target you and cast the spell on you without losing your target.

Just assign the macro's under a quick key.

## Activate:
```
/script setglobal("PWS","Power Word: Shield(Rank 10)"); setglobal("FH","Flash Heal(Rank 7)"); setglobal("H2","Heal(Rank 4)"); setglobal("DM","Dispel Magic(Rank 2)");
/nod
```

## Power word shield:
```
/script local p="player";t="target";if(not UnitCanAttack(t, p))then ot=UnitName(t); TargetUnit(p);else ot=nil;end;CastSpellByName(getglobal("PWS"));if(SpellIsTargeting()) then SpellTargetUnit(t);end;if(ot) then TargetByName(ot);end
```

## Flash Heal:
```
/script local p="player";t="target";if(not UnitCanAttack(t, p))then ot=UnitName(t); TargetUnit(p);else ot=nil;end;CastSpellByName(getglobal("FH"));if(SpellIsTargeting()) then SpellTargetUnit(t);end;if(ot) then TargetByName(ot);end
```

## Heal:
```
/script local p="player";t="target";if(not UnitCanAttack(t, p))then ot=UnitName(t); TargetUnit(p);else ot=nil;end;CastSpellByName(getglobal("H2"));if(SpellIsTargeting()) then SpellTargetUnit(t);end;if(ot) then TargetByName(ot);end
```

## Dispel Magic:
```
/script local p="player";t="target";if(not UnitCanAttack(t, p))then ot=UnitName(t); TargetUnit(p);else ot=nil;end;CastSpellByName(getglobal("DM"));if(SpellIsTargeting()) then SpellTargetUnit(t);end;if(ot) then TargetByName(ot);end
```

## >>>>>>>>>>>>>>>>>>edit 6/6<<<<<<<<<<<<<<<<<<<<
i just saw, that with patch 1.10, blizz introduced a new variable ,1
means there is no need anymore, for such complex macros like the ones above.
optimized for 1.10 all the self casting macros w/o loosing target look like this now. (also the "starter macro" above is obsolete now)

the macros are much easier now.
```
/script CastSpellByName("WHAT_EVER_U WANT_TO_CAST_ON_URSELF", 1)
```


## Renew Stopper
You always want to keep renew on tanks, but in raid groups you often accdently override other's Renew's wasting mana, This macro is to replace your renew key, and simply casts renew only if the target doesnt currently have it on. (Usually you can't cast renew on target if there is "A more powerfull spell already active". In the case Healers have all the same lvl, this will stop it if renew is already active active)
```
/script fred = 0 for i=1,16 do if UnitBuff("target", i) then if string.find(UnitBuff("target", i), "Renew") then fred = 1 end end end if fred == 0 then CastSpellByName("Renew") end
```

## Needy Heal
This macro will heal the person in your party who has the lowest health, and who isn't taking a dirtnap yet. Yes, just click the macro and the person with the least amount of health will be healed.
```
/script P=1;T="player";function F(a)h=UnitHealth(a);p=h/UnitHealthMax(a);if h>0 and P>p then P=p;T=a;end end F(T);for i=1,4 do p="party"..i;if p then F(p);end end TargetUnit(T);CastSpellByName("Holy Light(Rank ?)");TargetLastEnemy()
```

Remember to change the spell names and ranks, depending on your class and level. "Holy Light Rank ?" was used in the script above just to show proper placement.

This will also works for Druids too.

## Even More Fun with PI
```
/script c=UnitClass("target") nm=UnitName("target"); if ( c == "Mage" or c=="Priest" or c=="Warlock" or c=="Shaman" ) then CastSpellByName("Power Infusion"); SendChatMessage("You have Power Infusion!","WHISPER",nil,nm); end
```

im still looking for a method, to cast PI randomly in a raid on a mage/lock
like scan for caster, pick 1, cast PI
gimme a hand ppl




## Ressurection
simply says who u res
```
/script if UnitIsDeadOrGhost("target") then CastSpellByName("Resurrection"); SendChatMessage("Return to us, %t.","SAY"); end
```



## Shackle
Says what u shackle
```
/script CastSpellByName("Shackle Undead");
/script if UnitCreatureType("target") == "Undead" then SendChatMessage(">>> Shackling %t, leave it be.","SAY"); end
```



## Healing Rotation
This macro looks at your total mana and if you're at 10% mana or less, it alerts your healing rotation that you're out of mana and the next healer should step in. Otherwise, it will cast Flash Heal Rank 7.
```
/script p="player";m=UnitMana(p);mm=UnitManaMax(p);if (m < (mm/10)) then SendChatMessage("I am at 10% of my mana, next healer please take over.", "SAY") else CastSpellByName("FlashHeal(Rank 7)"); end
```

also possible to tell it in /ooshealers for instance, so druids can innverate, or someone takes over until u rec a bit


## Hot Button 4 Different Spells (Works for 1.10)
Apply four different spells to one hotkey using the control, alt or shift key. Change spells as desired, and change key positions depending on which one you want for the keys and as default.
(Note: on a Mac system, the shift key may not be usable for this... pending tests to confirm)
```
/script local d=CastSpellByName; if(IsControlKeyDown()) then d("Shadow Word: Pain") elseif (IsAltKeyDown()) then d("Smite") elseif (IsShiftKeyDown()) then d("Mind Blast") else d("Psychic Scream") end
```


## emergency heal with ct_raid
```
/script CT_RA_Emergency_TargetMember(1);
/cast Flash Heal(Rank 7)
/script ClearTarget();
```
 

Made by Tarantala 
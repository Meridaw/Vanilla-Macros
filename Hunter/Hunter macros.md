## AUTO SHOT
As strange as it might sound to have a macro for something as simple as Auto Shot, this is actually pretty important. Auto Shot is the core of your abilities, used for everything from initiating on a new target (before Aimed Shot) to doing most of your damage in dungeons and raids. 
```
/script if GetUnitName("target")==nil then TargetNearestEnemy() end
/run if CheckInteractDistance("target", 3) and (not PlayerFrame.inCombat) then AttackTarget() elseif not IsAutoRepeatAction(3) then CastSpellByName("Auto Shot") end
```


## This two-line macro will:
- Automatically target anything in front of you if you don't have a target.
- Begin using Auto Shot if you're at the appropriate distance to strike.
- Prevent Auto Shot from being toggled off if you hit the key again.
- Swap to melee auto attack if you're too close to Auto Shot.

Two important functions in particular are added: The automatic targeting, which will allow you to basically point and shoot with your right mouse and Auto Shot keybind, and the function that prevents Auto Shot from being toggled off. Auto Shot is on its own cooldown, independent of the GCD, so it's important to be able to enable it on demand.

You will need to modify this macro if you place it on any key other than 3 on your primary action bar. Please reference this screenshot:
![Alt text](http://i.imgur.com/VGArn.jpg)

And change the 3 in THIS part of the script:
```
IsAutoRepeatAction(3)
```
To the key corresponding with the location of the macro on your own interface.

## MELEE ATTACKS
This is just a basic macro to lump all of your offensive melee skills onto one bind.
``` 
/script if (not PlayerFrame.inCombat) then AttackTarget() end
/cast Raptor Strike
/cast Counterattack
/cast Mongoose Bite
```


The first line will begin your melee attack, regardless of distance to target. The next three lines cast abilities. Because Raptor Strike and Mongoose Bite function differently, they can be used simultaneously. Counterattack and Mongoose Bite cannot be used simultaneously, but Counterattack is a priority, so it's listed first.

## GENERAL SHOTS
Consider the macro below to be a default for all of your skill shots. This example casts Serpent Sting.
``` 
/script if GetUnitName("target")==nil then TargetNearestEnemy() end
/cast Serpent Sting
```


The first line is automatic targeting. The second line will cast your ability.

If you also wish to initiate your Auto Shot alongside your other shots, as I prefer, use the following macro instead... if you have an addon that allows longer than 255 characters.
``` 
/script if GetUnitName("target")==nil then TargetNearestEnemy() end
/cast Arcane Shot(rank 1)
/run if CheckInteractDistance("target", 3) and (not PlayerFrame.inCombat) then AttackTarget() elseif not IsAutoRepeatAction(3) then CastSpellByName("Auto Shot") end
```


Just don't forget to change "IsAutoRepeatAction(3)" to correspond with your interface again.

If you don't have an addon like that, use this one instead. The following shorter script will attempt to enable your Auto Shot, but will not switch to melee attack if you're too close to your target.
``` 
/script if GetUnitName("target")==nil then TargetNearestEnemy() end
/cast Arcane Shot(rank 1)
/script if not IsAutoRepeatAction(3) then CastSpellByName("Auto Shot"); end
```


## BASIC PET MACROS
Controlling your pet effectively is quite important. Your pet can aggro mobs, establish CC or break it, and ought to be doing damage on just the right target, or be in the right place to do that damage. So, this section will go over a few basic pet control macros and what you can do with them.

## PET ATTACK
The following macro is a simple macro that'll send your pet at your target. 
```
/script if GetUnitName("target")==nil then TargetNearestEnemy() end
/script CastPetAction(2);
/script CastPetAction(10);
/script PetAttack(target)
/cast Charge
/cast Dash
```


This macro's six lines do the following:
- Automatic targeting.
- Pet will follow you when disengaged from combat.
- Pet will act passively when disengaged from combat.
- Pet will attack the target specified.
- If available, your boar will Charge the target specified.
- If Charge isn't available or possible, Dash will be enabled instead.

One of the most useful scripts in this macro is the CastPetAction script. Your pet's action bar has 10 abilities on it, and Follow is on 2 by default and Passive is on 10 by default. Since Attack is ordered after these two lines, your pet will attack your target. The reason for setting your pet to follow and passive is that direct control over your pet's actions will help to prevent mistakes. When you need to give orders to your pet, it's best to have it under your complete control, so setting it to Follow and Passive every time you give an order is a safe default.

The final two lines contribute to your control. If you leave Dash on auto cast, your pet will spam it on cooldown, and that wastes focus and is likely to either prevent your pet from catching up to a target you need to catch, or get your pet killed if you need Dash to pull it back to you faster. By ordering Dash on attack, you ensure that your pet will make the fastest run to a new enemy target.

## PET FOLLOW
When you loose your pet on something, you're going to want some way to bring it back to you, for instance if the enemy flees and your pet will attract more enemies if it stays on that enemy. This macro does that:
 
```
/script PetFollow("Raziya")
/script CastPetAction(10);
/cast Dash
```


It's a very straightforward macro. Just change "Raziya" in between the parentheses to your name. The second line causes your pet to be passive, provided the passive command is in its default position on your pet's action bar, at 10. The third line will make your pet Dash back to you, which is convenient if you need to pull it out of danger quickly.

## PET STAY
Telling your pet to stay has various uses. You can use it to guard a flag, or fool people by Shadowmelding in a different bush than the one your pet is in, or maybe you need to leave it behind while you go pull the acolytes out of a Ziggurat in Strath UD. Whatever the case, having a keybind for your pet to stay is useful. Here it is:
 
```
/script CastPetAction(3);
/script CastPetAction(10);
```


The first line will tell your pet to stay. The second line will make your pet act passively.

## PET GROWL
You'll probably have your Growl turned off sometimes, like in a dungeon or for PvP. If an enemy rushes for your healer, you can send your pet at the enemy, order it to Growl, and then send it back at the mobs near the tank, effectively bringing the mob back to the tank spot without having to stop your DPS.
 
```
/cast Growl
/run local i,g=1,0 while GetSpellName(i,"pet") do if GetSpellName(i,"pet")=="Growl" then g=i end i=i+1 end local _,y = GetSpellAutocast(g,"pet") if not y then ToggleSpellAutocast(g,"pet") end
```


The first line commands your pet to Growl. The second line turns its auto cast on. If you want a script to turn Growl's auto cast off, one contributor posted this in the comments on this thread:
 

## Etrigan wrote:
```
/script local i,g=1,0 while GetSpellName(i,"pet") do if GetSpellName(i,"pet")=="Growl" then g=i end i=i+1 end local _,y = GetSpellAutocast(g,"pet") if (y and UnitFactionGroup("target")) then ToggleSpellAutocast(g,"pet") end
```


## MISCELLANEOUS MACROS
Here are just a couple of macros which don't fall under other categories. One of them is Night Elf-specific.

## FEIGN DEATH
This macro will ensure that the only time you ever use Feign Death is while you're in combat.
``` 
/script if UnitAffectingCombat("player") then CastSpellByName("Feign Death") end
```


On its own, it's nothing special, but this script will be used in combination with other abilities later.

## SHADOWMELD
Shadowmeld is a great skill that can help you stay alive or set up kills, especially as a hunter.
 
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Ability_Ambush" then x=1 end i=i+1 end if x==0 then CastSpellByName("Shadowmeld") else end
```


This will prevent you from toggling your Shadowmeld off. I don't know any sort of macro that would do the same for Prowl, so... sorry!

## DETERRENCE / MONKEY
```
/cast Deterrence
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Ability_Hunter_AspectOfTheMonkey" then x=1 end i=i+1 end if x==0 then CastSpellByName("Aspect of the Monkey") else end
```


This Deterrence macro will cast Aspect of the Monkey and Deterrence. Aspect of the Monkey will not be toggled off.
 

## FRIEND OR FOE
This script will cast one spell if your target is friendly. It'll cast a different spell if your target is hostile.
```
/script if UnitIsFriend("player", "target") then CastSpellByName("Aspect of the Pack") else CastSpellByName("Aspect of the Cheetah") end
```


This example will cast Pack if your target is friendly, but Cheetah under any other circumstances. That way, if you're in a group and you want to give Pack to people, just click an ally and you don't have to reserve another keybind for Pack!

You can modify this to use items. For instance, here's my Scare Beast macro:
``` 
/script if GetUnitName("target")==nil then TargetNearestEnemy() end
/script if UnitIsFriend("player", "target") then UseContainerItem(0, 16) else CastSpellByName("Scare Beast") end
```


If targeting an ally, this will use the item in the lower-right corner of my backpack. That's where I keep my bandages. Experiment with the UseContainerItem parameters as needed.

## CC MACROS
Hunters have incredible crowd control, but several of our abilities can be tricky to use, such as traps, which require we be out of combat. I put together these macros to help make CC more easily maintained.

## SCATTER SHOT MACRO
This macro is awesome for abilities like Scatter Shot or Wyvern Sting.
``` 
/script if GetUnitName("target")==nil then TargetNearestEnemy() end
/script if UnitExists("pettarget") and UnitIsUnit("target", "pettarget") then PetPassiveMode() CastPetAction(3); else end
/cast Scatter Shot
```


After auto targeting, this macro will check if you and your pet are attacking the same target. If so, your pet will be set to passive and stay at its current position. If not, your pet will continue attacking its target.

Just remember to give the attack order again after your enemy has recovered.

## FEIGN DEATH / TRAP
Since hunters can't use traps in combat, we need to rely on Feign Death to drop a trap in a pinch. This macro has proven to be very useful:
``` 
/cast Immolation Trap
/script if UnitAffectingCombat("player") then CastSpellByName("Feign Death") end
```


You need to hit this macro at least twice regardless of script order, so you might as well have your trap as the first line so your macro shows the tooltip for the trap, rather than Feign Death.

## FREEZING TRAP
The Freezing Trap can be broken by your pet too, so I went ahead and did this to mine:
``` 
/cast Freezing Trap
/script if UnitAffectingCombat("player") then CastSpellByName("Feign Death") end
/script if UnitExists("pettarget") and CheckInteractDistance("target", 3) and UnitIsUnit("target", "pettarget") then PetPassiveMode(); else end
```


Feign Death will be used if you're in combat. If you and your pet are targeting the same thing, and the enemy is close to you, then your pet will be pulled off of the enemy. The only drawback is that you'd need to be targeting the enemy you intend to trap, but in a 1v1 this works nicely. So, world PvP.

## ADVANCED MACROS
Here we get into some longer, cooler macros than the basic ones mentioned before this point. All of them will be focused on reducing keybinds based on situational parameters.

## COMBAT ASPECT SWAP / ASPECT SITUATIONAL
Aspect of the Hawk and Aspect of the Monkey are both important abilities to have bound, especially for a PvPer or a Ravager, but you'd need two keybinds. The following macros put them in one keybind.

The first solution I came up with was a swap macro:
``` 
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Nature_RavenForm" then x=1 end i=i+1 end if x==0 then CastSpellByName("Aspect of the Hawk") else CastSpellByName("Aspect of the Monkey") end
```


This macro uses a similar structure to the Shadowmeld macro. If you're in no aspect or in any other aspect, it'll toggle on Aspect of the Hawk. If you're in Aspect of the Hawk, it'll switch to Aspect of the Monkey.

The second solution I came up with was a distance check:
``` 
/run if CheckInteractDistance("target", 3) then CastSpellByName("Aspect of the Monkey") else CastSpellByName("Aspect of the Hawk") end
```


This macro uses a similar structure to the Auto Shot macro. If you have no target or if your target is far away from you, it'll cast Aspect of the Hawk. If your target is close to you, it'll cast Aspect of the Monkey.

Both macros function differently, but to the same end. Take whichever you like, if either.

## SITUATIONAL STING
You're never going to use Scorpid Sting on a mage, right? Or Viper Sting on a rogue. So, here's a macro that casts the right sting depending on the class of your target:
``` 
/script if GetUnitName("target")==nil then TargetNearestEnemy() end
/script class=UnitClass("target"); if ((class=="Rogue") or (class=="Warrior")) then CastSpellByName("Scorpid Sting"); else CastSpellByName("Viper Sting"); end
```


It also seems to work on NPCs. NPCs with mana get Viper Sting, and NPCs without mana get Scorpid Sting. Reportedly a few people have had trouble with it on druids shapeshifted into cat or bear form, but I think that may have been an issue on Nostalrius only. On Kronos II I've confirmed that this works properly all the time.

## ALL-IN-ONE PET MAINTENANCE
We have a lot of abilities that affect our pet. The following macro combines feed pet, call pet, dismiss pet, and revive pet.
``` 
/run local c=CastSpellByName if UnitExists("pet") then if UnitHealth("pet")==0 then c("Revive Pet") elseif GetPetHappiness()~=nil and GetPetHappiness()~=3 then c("Feed Pet") PickupContainerItem(0, 13) else c("Dismiss Pet") end else c("Call Pet") end
```


If your pet is dismissed, this macro will call it. If your pet is called and happy, this macro will dismiss it. If your pet is called and unhappy, this macro will feed it the item in the bottom left corner of your backpack. If your pet's dead, it'll be revived.

You can change the bagslot this macro checks for food in by changing the "PickupContainerItem(0, 13)" part. The bags count from 0-4, starting from the Backpack, so 0, 13 there means the 13th slot in the backpack.

## MY PERSONAL MACROS
Due to popular demand, I'm dropping a few of my own personal macros here. See details below:

## MULTI-SHOT
```
/script if GetUnitName("target")==nil then TargetNearestEnemy() end
/cast Multi-Shot(rank 1)
/cast Volley
/script if not IsAutoRepeatAction(3) then CastSpellByName("Auto Shot"); end
```


This is a simple fall-through macro. If you hit it once, you target anything up to 40 yards in front of you, cast Multi-Shot, and toggle your Auto Shot on. Hit it again while Multi-Shot is on cooldown, and you'll cast Volley. Alternatively, if Multi never goes off, Volley will be selected immediately.

Unless your Flare is on cooldown and you have the mana to spare to take a rogue out of invisibility, I don't really think you'll have any urgency to use Volley until you're AoEing something, and Multi-Shot is often the priority, hence the use of this macro.

Remember to adjust the Auto Shot script according to your interface. See section 2.2.1 for more information.

## WING CLIP
```
/script if (not PlayerFrame.inCombat) then AttackTarget() end
/cast Counterattack(Rank 1)
/cast Wing Clip
/cast Wing Clip(Rank 2)
/cast Wing Clip(Rank 1)
```


This is a fall-through macro for Wing Clip. If you happen to be super low on mana for some reason and can't use maximum rank Wing Clip, a lower rank will be used instead. Counterattack is a priority over all ranks of Wing Clip.

## COORDINATES
```
/script SetMapToCurrentZone() local x,y=GetPlayerMapPosition("player") DEFAULT_CHAT_FRAME:AddMessage(format("%s, %s: %.1f, %.1f",GetZoneText(),GetSubZoneText(),x*100,y*100))
```
This macro tells you your current coordinates. I keep it around to help mark locations on my map using Cartographer's note system.

 

Macros by Raziya
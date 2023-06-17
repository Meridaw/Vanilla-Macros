## Fakecasting without having to move character:
```
/run SpellStopCasting()
```
 
## Fire Blast specific Enemy
Cast fireblast on enemy that matches name below EXACTLY. Useful when lvling to tag mobs first.
```
/run TargetByName("REPLACE THIS TO NPC NAME", true) CastSpellByName("Fire Blast")
```
 
## Prevent wand / autoattack toggling 
Script to prevent toggling of wand/autoattack + green targeting reticle.
You only need to run this once every login. Remove "/run" and copy into an addon lua file if you're lazy.:
```
/run local _UseAction = UseAction;UseAction=function(id,a,b)if not IsCurrentAction(id)and not IsAutoRepeatAction(id)and not SpellIsTargeting()then _UseAction(id, a, b)end end
```
 
 
## Fast Counterspell 
stops your cast before using ability
```
/run SpellStopCasting() CastSpellByName("Counterspell")
```
 
 
## Fast Cold Snap:
```
/run SpellStopCasting() CastSpellByName("Cold Snap")
```
 
 
## Fast Ice Block
```
/run SpellStopCasting() CastSpellByName("Ice Block")
```
 
## Fast blink:
```
/run SpellStopCasting() CastSpellByName("Blink")
```
 
 
## Use rank1 Fire Blast if target is totem, else highest rank. (UNTESTED):
```
/run local target=GetUnitName("target")if target and string.find(target,"Totem")then CastSpellByName("Fire Blast(rank 1)") else CastSpellByName("Fire Blast")end
```
 
 
## ** Macros below are mostly useful for saving actionbar space **
 
## 1 Button Fireball/scorch (will also use wand when locked on fire school)
If you don't have a wand, I think this macro will bug out, but you can just remove "/cast Shoot" at the end.<br/>
SHIFT + KEYBINDING = Fireball<br/>
KEYBINDING = Scorch<br/>
```
/run CastSpellByName(IsShiftKeyDown() and "Fireball" or "Scorch")
/cast Shoot
```
 
Note that if modifier + keybinding is already keybound to something different, this macro won't work. You'll need to unbind it first.
Also pressing modifier + modifier + keybinding wont work. So you can't keybind this macro to "SHIFT+1" for example, but "1" would work.
 
 
## 1 Button wards
SHIFT + KEYBINDING = Fire Ward<br/>
KEYBINDING = Frost Ward<br/>
```
/run CastSpellByName(IsShiftKeyDown() and "Fire Ward" or "Frost Ward")
```
 
 
## Frostbolt with downrank
SHIFT + KEYBINDING = rank1 frostbolt for fast slow<br/>
KEYBINDING = highest frostbolt rank available<br/>
Will also retarget last enemy if u lose it (i.e when a hunter uses feign death)<br/>
```
/run if not UnitExists("target")then TargetLastEnemy()end CastSpellByName(IsShiftKeyDown() and "Frostbolt(rank 1)" or "Frostbolt")
```
 
 
## Arcane Explosion with downrank (great for catching stealthers)
SHIFT + KEY = r1 Arcane Explosion<br/>
KEY = highest rank<br/>
```
/run CastSpellByName(IsShiftKeyDown() and "Arcane Explosion(rank 1)" or "Arcane Explosion")
```
 
I also recommend copying the above macro and creating seperate versions for Fireball, Cone of Cold, Flamestrike and Blizzard.
You might also want to do it with certain buffs for dispel protection when playing with pom/ice barrier.
 
 
## 1 Button Buff (except Amplify Magic)
SHIFT + KEYBINDING = Ice Armor (not frost armor!)<br/>
CTRL + KEYBINDING = Dampen Magic<br/>
ALT + KEYBINDING = Mage Armor<br/>
KEYINDING = Arcane Intellect<br/>
```
/run CastSpellByName(IsShiftKeyDown() and "Ice Armor" or IsControlKeyDown() and "Dampen Magic" or IsAltKeyDown() and "Mage Armor" or "Arcane Intellect")
```
 

Made by reflect
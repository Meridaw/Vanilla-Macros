## This will Innervate weapon swap if you put your +spirit staff in the 1st slot of your backpack
```
/script UseContainerItem(0,1)
/script TargetUnit("player")
/cast Innervate
/script TargetLastTarget()
```
 

## Innervate on yourself and retarget last target
```
/script TargetUnit("player")
/cast Innervate
/script TargetLastTarget()
```
 

## No double-innervate (Useful for raids)
```
/run t="target" p="player" b="Innervate" if (UnitIsFriend(p,t) and UnitManaMax(t)>200) then for i=1,16 do if UnitBuff(t,i) then if not string.find(UnitBuff(t,i), b) then CastSpellByName(b) end end end else ChatFrame1:AddMessage("Did not "..b.."!") end
```


## Innervate and whisper to target
```
/cast Innervate
/run if UnitExists"target"then SendChatMessage("flavor text","WHISPER",nil,UnitName"target")end
```


## Innervate overwrite prevention

Allows you to check if Innervate is already active on your target. This does conflict with mage arcane power as it uses the same spell icon. It’s not a big issue though but keep it in mind.

Really useful if you’re raiding together with several druids. Make sure that everyone use it and you will never waste an innervate again!
```
/run n=0 for i=1,40 do if(strfind(tostring(UnitBuff("target",i)),"Spell_Nature_Lightning"))then n=1 end end if n==0 then CastSpellByName("Innervate")end
```

Its also useful to combine with a whisper or a broadcast in your guild healing channel or raid chat. Unfortunately using LUA functions will far surpass the 255 character limit so just add this:
```
/w %t <<INNERVATING>> you!
/5 <<INNERVATING>> %t!
```
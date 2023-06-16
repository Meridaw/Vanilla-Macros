## Uses any bandage without losing target
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Bandage"))then UseContainerItem(b,s)SpellTargetUnit("player")end end end
```
 

## Bandage self without losing combo points. My bandages are located in slot 1 of my backpack.
```
/script UseContainerItem(0, 1)
/script SpellTargetUnit("player")
```
 

## Pvp Bandage macro
```
/script TargetUnit("Player")
/script UseContainerItem(x,y)
/script TargetLastEnemy();
```

## Pve Bandage macro
```
/script TargetUnit("Player")
/script UseContainerItem(x,y)
/assist TargetUnit("Maintank")    <----- replace Maintank with the name of you tank
```
x = The bag<br/>
y = The slot of the bag<br/>
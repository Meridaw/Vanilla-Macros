## AQ40 Mount combined with regular mount – all in one macro

This macro will look for the name “Qiraji Res” through your bags and use that if you’re currently in the zone Ahn’Qiraj. As there are a lot of mounts to choose from you will need to edit the name of your regular mount that you want it to use when outside the instance. Here are some examples.

## Macro to copy and paste if you have a Raptor Mount
```	
/run function u(n)for b=0,4 do for s=1,GetContainerNumSlots(b)do a=GetContainerItemLink(b,s)if a then if string.find(a,n)then UseContainerItem(b,s)return end end end end end if GetZoneText()=="Ahn'Qiraj"then u("Qiraji Res")else u("Whistle of")end
```


## Macro to copy and paste if you have a Wolf Mount
```	
/run function u(n)for b=0,4 do for s=1,GetContainerNumSlots(b)do a=GetContainerItemLink(b,s)if a then if string.find(a,n)then UseContainerItem(b,s)return end end end end end if GetZoneText()=="Ahn'Qiraj"then u("Qiraji Res")else u("Horn of")end
```


## Macro to copy and paste if you have an Undead Horse
```	
/run function u(n)for b=0,4 do for s=1,GetContainerNumSlots(b)do a=GetContainerItemLink(b,s)if a then if string.find(a,n)then UseContainerItem(b,s)return end end end end end if GetZoneText()=="Ahn'Qiraj"then u("Qiraji Res")else u("Skeletal War")end
```

For Kodos or other you mounts you need to edit the last part of the macro
You need to edit u(“Teal Kodo“) part to for example u(“Brown Kodo“) or u(“Reins of“) or u(“Skeletal Hors“).

The whole name probably wont fit in the 255 character limit unless you have a long macro addon like Supermacro installed.

WARNING BE VERY CAREFUL not to add something that might match the name of an important consume like “Distilled” or “Supreme” or the like!


Made by Sandsten
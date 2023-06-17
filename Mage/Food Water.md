## Uses any Conjured water/food (press it quick twice, to eat when you drink)
```
/run for b=0,4 do for s=1,GetContainerNumSlots(b,s)do local n=GetContainerItemLink(b,s)if n and (strfind(n,"Conjured"))then UseContainerItem(b,s,1)end end end
```
 

## Conjured Water

Casts the highest rank Water available for the friendly target.

Because this script uses spell numbers instead of names, you will need to customize the script to fit your character. There is an small script you can use to help determine spell numbers. For the script found below, you will need to use one spell lower then Conjure Water Rank 1. For example, Conjure Water Rank 1 was spell number 51. I must use spell number 50 in my script.

Line breaks (carriage returns or <Enter>) have been added for legibility only. When copied into WoW, make sure the script is one line only.
```
/script L={1,5,15,25,35,45,55} if (UnitLevel("target") ~= nil) then for i=7,1,-1 do if (UnitLevel("target") >= L) then CastSpell(50+i,"spells"); return; end; end; end;
```
 

Alternatively, if you wish to use spell names, the following script is based on a Fortitude example.
```
/script Pre="Conjure Water(Rank "; Sp={1,5,15,25,35,45,55} if (UnitLevel("target") ~= nil) then for i=7,1,-1 do if (UnitLevel("target") >= Sp) then CastSpellByName(Pre..i..")"); return; end; end; end;
```
 

This version is similar to the above one, but if you have no target or if the alt key is held down, it will cast appropriately to your own level.
```
/script c=CastSpellByName t=UnitLevel("target") Pre="Conjure Water" Sp={1,5,15,25,35,45,55} if (IsAltKeyDown() or t<1) then c(Pre) else for i=7,1,-1 do if (t>=Sp) then c(Pre.."(Rank "..i..")"); return; end; end; end
```
 

 
## Conjured Food

Casts the highest rank Food available for the friendly target.

Because this script uses spell numbers instead of names, you will need to customize the script to fit your character. There is an small script you can use to help determine spell numbers. For the script found below, you will need to use one spell lower then Conjure Food Rank 1. For example, Conjure Food Rank 1 was spell number 41. I must use spell number 40 in my script.

Line breaks (carriage returns or <Enter>) have been added for legibility only. When copied into WoW, make sure the script is one line only.
```
/script L={1,5,15,25,35,45} if (UnitLevel("target") ~= nil) then for i=6,1,-1 do if (UnitLevel("target") >= L) then CastSpell(40+i,"spells"); return; end; end; end;
```
 

Alternatively, if you wish to use spell names, the following script is based on a Fortitude example.
```
/script Pre="Conjure Food(Rank "; Sp={1,5,15,25,35,45} if (UnitLevel("target") ~= nil) then for i=6,1,-1 do if (UnitLevel("target") >= Sp) then CastSpellByName(Pre..i..")"); return; end; end; end;
```
 

This version is the same as the above, but when you have no target or you hold down the alt key it will conjure appropriately to you.
```
/script csb=CastSpellByName t=UnitLevel("target") Pre="Conjure Food"; Sp={1,5,15,25,35,45} if (IsAltKeyDown() or t<1) then csb() else for i=6,1,-1 do if (t >= Sp) then csb(Pre.."(Rank "..i..")"); return; end; end; end;
```
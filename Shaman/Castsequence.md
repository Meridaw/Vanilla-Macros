## Windfury, Strenght of Earth, Mana Spring
```
/run local _gspells = { "Windfury Totem", "Strength of Earth Totem", "Mana Spring Totem"} if GetSpellCooldown(4,"BOOKTYPE_SPELL")==0 then _gi=_gi and _gi > 0 and _gi or 1 CastSpellByName(_gspells[_gi]) _gi = math.mod(1+_gi, 1+table.getn(_gspells))end
```
 

## Windfury, Strenght of Earth, Mana Spring
```
/run s={"Windfury Totem","Strength of Earth Totem","Mana Spring Totem"} if q==nil then q=0 end q=q+1 if q>getn(s) then q=1 end CastSpellByName(s[q])
```


## Re-popping totems using the cheapest rank 1 spells 
Clicking faster than the global cooldown will skip totems
```
/run s={"Fire Resistance Totem(Rank 1)","Nature Resistance Totem(Rank 1)","Stoneskin Totem(Rank 1)","Frost Resistance Totem(Rank 1)"} if q==nil then q=0 end q=q+1 if q>getn(s) then q=1 end CastSpellByName(s[q])
```


## Searing / Strength of Earth / Healing Stream
```
/run c=CastSpellByName if n==0 then c("Searing Totem") n=1 elseif n==1 then c("Strength of Earth Totem") n=2 else c("Healing Stream Totem") n=0 ;end
```
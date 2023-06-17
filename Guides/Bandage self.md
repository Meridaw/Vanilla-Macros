## Bandage self with Autoselfcasting disabled

This macro works without any addons and you can have the bandage placed anywhere in your bags.

It looks for items with the word “Bandage” in your bags starting in bag 0 so if the macro uses the wrong bandage before the Heavy Runecloth, move Heavy Runecloth into bag 0 (your backpack). Here is a list with bandages it should work with:
```
1251 - Linen Bandage
2581 - Heavy Linen Bandage
3530 - Wool Bandage
3531 - Heavy Wool Bandage
6450 - Silk Bandage
6451 - Heavy Silk Bandage
8544 - Mageweave Bandage
8545 - Heavy Mageweave Bandage
9332 - Crusted Bandages
14529 - Runecloth Bandage
14530 - Heavy Runecloth Bandage
16112 - Manual: Heavy Silk Bandage
16113 - Manual: Heavy Mageweave Bandage
16991 - Triage Bandage
19066 - Warsong Gulch Runecloth Bandage
19067 - Warsong Gulch Mageweave Bandage
19068 - Warsong Gulch Silk Bandage
19307 - Alterac Heavy Runecloth Bandage
20065 - Arathi Basin Mageweave Bandage
20066 - Arathi Basin Runecloth Bandage
20067 - Arathi Basin Silk Bandage
20232 - Defiler's Mageweave Bandage
20234 - Defiler's Runecloth Bandage
20235 - Defiler's Silk Bandage
20237 - Highlander's Mageweave Bandage
20243 - Highlander's Runecloth Bandage
20244 - Highlander's Silk Bandage
```
It works with autoselfcasting disabled in options (for the addon Clique to function) and will keep your current target.
```	
/run TargetUnit("player")function u(n)for b=0,4 do for s=1,GetContainerNumSlots(b)do a=GetContainerItemLink(b,s)if a then if string.find(a,n)then UseContainerItem(b,s,1)return end end end end end u("Bandage")TargetLastTarget()
```

Made by Sandsten
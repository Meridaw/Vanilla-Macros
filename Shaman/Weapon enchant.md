## Weapon ﻿imbu﻿﻿e specific weapon 
edit NameOfWeapon to the specific weapon you want to imbue
```
/run if string.find(GetInventoryItemLink("player",16), "NameOfWeapon") then CastSpellByName("WeaponImbueSpellName") end
```

## Enchant Rockbiter Weapon on mainhand, else cast Lightning Shield
```
/run hasMainHandEnchant, mainHandExpiration = GetWeaponEnchantInfo() if  not hasMainHandEnchant then CastSpellByName("Rockbiter Weapon")else CastSpellByName("Lightning Shield")end
```
 

## Enchant Rockbiter Weapon on mainhand, start attack, else cast Lightning Shield
```
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z)end;end;end;hasMainHandEnchant =GetWeaponEnchantInfo()if  not hasMainHandEnchant then CastSpellByName("Rockbiter Weapon")else CastSpellByName("Lightning Shield")end
```
 

## Enchant Rockbiter Weapon on mainhand, start attack, else cast Searing Totem
```
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z)end;end;end;hasMainHandEnchant =GetWeaponEnchantInfo()if  not hasMainHandEnchant then CastSpellByName("Rockbiter Weapon")else CastSpellByName("Searing Totem")end
```
 

## Enchant Windfury Weapon, start attack, else cast Fire Nova Totem
```
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z)end;end;end;hasMainHandEnchant =GetWeaponEnchantInfo()if  not hasMainHandEnchant then CastSpellByName("Windfury Weapon")else CastSpellByName("Fire Nova Totem")end
```
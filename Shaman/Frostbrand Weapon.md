## Frostbrand Weapon / Auto Attack
```
/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z)end;end;end;hasMainHandEnchant =GetWeaponEnchantInfo()if  not hasMainHandEnchant then CastSpellByName("Frostbrand Weapon")end UIErrorsFrame:Hide()
```
## Disable audio for macro to cast spell
```
/console Sound_EnableSFX 0
/script if GetUnitName("target")==nil then TargetNearestEnemy() end
/cast Fireball
/console Sound_EnableSFX 1
/script UIErrorsFrame:Clear();
```
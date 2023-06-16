## Bloodrage + cancel buff
```
/script local i=0 g=GetPlayerBuff while not (g(i) == -1) do if(strfind(GetPlayerBuffTexture(g(i)),"Ability_Racial_BloodRage"))then CancelPlayerBuff(g(i)) end i=i+1 end CastSpellByName("Bloodrage")
```


## Bloodrage -> Battle Stance -> Sweeping Strikes
```
/cast Bloodrage
/script texture,name,isActive,isCastable = GetShapeshiftFormInfo(1); if isActive then CastSpellByName("Sweeping Strikes"); else CastSpellByName("Battle Stance()"); end;
```
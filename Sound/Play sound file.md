## Play the RaidWarning sound
```
/run PlaySound ("RaidWarning");
```


## Play RaidWarning sound if target exist
```
/run if UnitExists("target") then PlaySound ("RaidWarning"); else end
```


## Check that you have proper druid HoTs on you
```
/script local i=0 g=GetPlayerBuff while not(g(i) == -1)do if(strfind(GetPlayerBuffTexture(g(i)), "Spell_Nature_Rejuvenation"))then PlaySoundFile("Sound\Creature\Ossirian\OssirianIAmRejuvenated.wav")end i=i+1 end
```
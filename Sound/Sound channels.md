## Enter each of these commands in-game and then restart your client.
```
/console SoundMemoryCache 128
/console SoundMaxHardwareChannels 128
/console SoundSoftwareChannels 128
```
put compatibility option to XP SP3 if you get sound issues

 

## You can add this one if you want too:
```
/console SoundMixRate 48000
```
 

## Set in game:
```
/run SetCVar("Sound_NumChannels",128)
```
## Confirm its done:
```
/dump GetCVar("Sound_NumChannels")
```
You can add 2 lines to your config.wtf - that way you dont need a modified .exe - the lines to add are SET SoundMaxHardwareChannels "256" and "SET SoundSoftwareChannels "256" - change the number 256 to the channels you want. I have it set to the max of 256. 
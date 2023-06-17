## If youve got your 4 mounts in the first 4 slots of your first bag it would look like this
```
/script UseContainerItem(0,math.random(1,4));
```
 

## Dismount, summon random mount
```
/run local i=0 g=GetPlayerBuff while not(g(i) == -1)do if(strfind(GetPlayerBuffTexture(g(i)), "Ability_Mount"))then CancelPlayerBuff(g(i))end i=i+1 end
/run UseContainerItem(0,math.random(1,4));
```
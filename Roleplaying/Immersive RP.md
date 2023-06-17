## Taunt:
```
/cast taunt
/run TeM=TeM or GetTime()-3 if (GetTime()-TeM)>3 and DoEmote("taunt") then TeM=GetTime() end
```


## Mocking Blow:
```
/cast Mocking Blow
/run TeM=TeM or GetTime()-3 if (GetTime()-TeM)>3 and DoEmote("taunt") then TeM=GetTime() end
```


## Charge:
```
/cast charge 
/run TeM=TeM or GetTime()-5 if (GetTime()-TeM)>5 and DoEmote("charge") then TeM=GetTime() end
```


## Intercept:
```
/cast Intercept
/run TeM=TeM or GetTime()-5 if (GetTime()-TeM)>5 and DoEmote("charge") then TeM=GetTime() end
```


## Battle Shout:
```
/cast battle shout
/run TeM=TeM or GetTime()-3 if (GetTime()-TeM)>3 and DoEmote("cheer") then TeM=GetTime() end
```


## Demoralizing Shout:
```
/cast Demoralizing Shout
/run TeM=TeM or GetTime()-3 if (GetTime()-TeM)>3 and DoEmote("laugh") then TeM=GetTime() end
```


## Challenging Shout:
```
/cast Challenging Shout
/run TeM=TeM or GetTime()-3 if (GetTime()-TeM)>3 and DoEmote("roar") then TeM=GetTime() end
```


## Intimidating Shout:
```
/cast Intimidating Shout
/run TeM=TeM or GetTime()-3 if (GetTime()-TeM)>3 and DoEmote("threaten") then TeM=GetTime() end
```


## Ranged Attack
```
/cast auto shot
/run TeM=TeM or GetTime()-3 if (GetTime()-TeM)>3 and DoEmote("incoming") then TeM=GetTime() end
```


## Last Stand
```
/cast Last Stand
/run TeM=TeM or GetTime()-3 if (GetTime()-TeM)>3 and DoEmote("healme") then TeM=GetTime() end
```


## Execute
```
/cast Execute
/run TeM=TeM or GetTime()-5 if (GetTime()-TeM)>5 and DoEmote("threaten") then TeM=GetTime() end
```


## Sunder
```
/cast sunder armor
/run TeM=TeM or GetTime()-5 if (GetTime()-TeM)>5 and DoEmote("attacktarget") then TeM=GetTime() end
```


## Defensive Stance 
```
/cast Defensive Stance
/run TeM=TeM or GetTime()-5 if (GetTime()-TeM)>5 and DoEmote("follow") then TeM=GetTime() end
```


## Hamstring
```
/cast Hamstring
/run TeM=TeM or GetTime()-5 if (GetTime()-TeM)>5 and DoEmote("wait") then TeM=GetTime() end
```


## War Stomp
```
/cast War Stomp
/run TeM=TeM or GetTime()-2 if (GetTime()-TeM)>2 and DoEmote("roar") then TeM=GetTime() end
```
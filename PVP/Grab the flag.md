## Announce to Grab the Flag
If the target HP is below 20 % remind the people to Grab the flag, and not only kill it! 
```
/script if (UnitHealth('target')/UnitHealthMax('target')<0.20) then SendChatMessage("target has under 20 % Health, BE READY TO GRAB FLAG","PARTY"); end
```
## Buff / Debuff Duration
shows your buff/debuff durations in seconds.
```
/run for i=0,31 do local id,cancel = GetPlayerBuff(i,"HELPFUL|HARMFUL|PASSIVE"); if(id > -1) then local timeleft = GetPlayerBuffTimeLeft(id); DEFAULT_CHAT_FRAME:AddMessage(timeleft); end end
```
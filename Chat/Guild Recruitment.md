## Guild Recruitment
```
/run n=GetNumWhoResults(); i=1; while(i<n+1) do c,g=GetWhoInfo(i); if(g=="") then SendChatMessage("Hello "..c.."! <GUILDNAME> is now recruiting!Awsome guild!, join now!","WHISPER","COMMON",c); GuildInvite(c); end; i=i+1; end;
```
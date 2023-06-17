## Drunk toggle macro 
useful for the zg spiders
```
/run local c,m=GetCVar("ffxGlow"),message if c=="1" then SetCVar("ffxGlow","0")m("Drunk GFX OFF")else SetCVar("ffxGlow","1")m("Drunk GFX ON")end
```
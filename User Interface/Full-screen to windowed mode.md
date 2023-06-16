## SwitchMode:
```
/run currentRes = GetCurrentResolution(); if (currentRes == 3) then SetScreenResolution(15); SetCVar("gxWindow", 0); SetMultisampleFormat(16);else SetCVar("gxWindow", 1); SetScreenResolution(3); SetMultisampleFormat(1); end;
```

Replace the 15 in SetScreenResolution with your selected high-res index, the 16 in SetMultisampleFormat with your selected colour depth/anti-aliasing, and the 3 in Set/GetScreenResolution with your preferred windowed res. To finish this one off, drop it into a popup button and go to key bindings, link in “alt-enter”. That way, alt-enter will alternate between windowed and full-screen. You can also work in any of the above Farclip etc calls to further alter the settings between windowed and full-screen, depending on how your machine behaves – experiment and see.
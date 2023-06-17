## Show the Battlefield Minimap outside of BGs
```
/run if(not BattlefieldMinimap)then BattlefieldMinimap_LoadUI()BattlefieldMinimap:Show()else BattlefieldMinimap:Show()end;SHOW_BATTLEFIELD_MINIMAP="1";
```
If you want to make it bigger append this at the end of the macro. 1.5 = 50% bigger, adjust as needed. All should be one line.
```
BattlefieldMinimap:SetScale(1.5);
```
## Movable Player Frame 
enable or disable moving for player frame
```
/run if not m then PlayerFrame:SetMovable(1)PlayerFrame:StartMoving()m=true else PlayerFrame:StopMovingOrSizing()PlayerFrame:SetMovable()m=false end
```


## Move player unit frame
```
/script PlayerFrame:SetMovable(1)PlayerFrame:StartMoving()
```


## Stop moving player unit frame
```
/script PlayerFrame:StopMovingOrSizing()PlayerFrame:SetMovable()
```


## Use these scripts to move player and target frame 
Adjust the coordinates to your liking.
```
/run PlayerFrame:ClearAllPoints() PlayerFrame:SetPoint("CENTER",UIParent,-150,-150)PlayerFrame:SetUserPlaced(true)
/run TargetFrame:ClearAllPoints() TargetFrame:SetPoint("CENTER",UIParent,150,-150)TargetFrame:SetUserPlaced(true)
```
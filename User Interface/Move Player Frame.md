## Move player unit frame
```
/script PlayerFrame:SetMovable(1)PlayerFrame:StartMoving()
```


## Stop moving player unit frame
```
/script PlayerFrame:StopMovingOrSizing()PlayerFrame:SetMovable()
```


## Move target unit frame
```
/script TargetFrame:SetMovable(1)TargetFrame:StartMoving()
```


## Stop moving target unit frame
```
/script TargetFrame:StopMovingOrSizing()TargetFrame:SetMovable()
```


## Use these scripts to move player and target frame 
Adjust the coordinates to your liking.
```
/run PlayerFrame:ClearAllPoints() PlayerFrame:SetPoint("CENTER",UIParent,-150,-150)PlayerFrame:SetUserPlaced(true)
/run TargetFrame:ClearAllPoints() TargetFrame:SetPoint("CENTER",UIParent,150,-150)TargetFrame:SetUserPlaced(true)
```
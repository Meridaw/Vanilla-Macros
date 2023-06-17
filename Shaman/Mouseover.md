## Mouseover Healing Wave
```
/run if UnitExists("mouseover") then TargetUnit("mouseover"); CastSpellByName("Healing Wave"); TargetUnit("playertarget") else CastSpellByName("Healing Wave") end
```


## Lesser Healing Wave on Mouseover if exist, else on selected target
```
/run s="Lesser Healing Wave" m="mouseover" T=TargetUnit C=CastSpellByName if UnitExists(m) then T(m) C(s) T("playertarget") else C(s) end
```


## Lesser Healing Wave on mouseover target if friendly, else on player
```
/run s="Lesser Healing Wave" m="mouseover" T=TargetUnit C=CastSpellByName if UnitExists(m) and UnitIsFriend("player", m) then T(m) else T("player")end C(s) T("playertarget")
```
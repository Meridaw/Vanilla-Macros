## Rank 1 Consecration, max rank if combat
```
/run if not UnitAffectingCombat("player") then CastSpellByName("Consecration(Rank 1)") else CastSpellByName("Consecration") end
```


## PvP Off
turns off pvp and uses rank 1 Consecration until you are no longer flagged for PvP
```
/run if not pvpTime then pvpTime = 0 end if UnitIsPVP("player") then CastSpellByName("Consecration(Rank 1)") end if pvpTime == 0 and UnitIsPVP("player") then TogglePVP() pvpTime = GetTime() end if GetTime() - pvpTime > 300 then pvpTime = 0 end
```
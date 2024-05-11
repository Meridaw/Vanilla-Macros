## Spammable Arcane Missiles
Using Arcane Missiles repeatedly is a DPS loss because of the way the spell works, so you need this complicated macro to gain an extra tick of the spell
```
/run local f=CnlSpam if not f then f=CreateFrame("Frame")local s,r="SPELLCAST_CHANNEL_ST",f.RegisterEvent r(f,s.."ART")r(f,s.."OP")f:SetScript("OnEvent",function()this.c=event~=s.."OP"end)CnlSpam=f end if not f.c then CastSpellByName("Arcane Missiles")end
```


## Spammable Arcane Missiles
```
/script if not CastingBarFrame.channeling then CastSpellByName("Arcane Missiles") end
```


## Spammable Arcane Missiles
```
/run if(CastingBarFrame.casting ~= 1 and CastingBarFrame.channeling ~= 1) then CastSpellByName("Arcane Missiles"); end;
```
 

## Throw rank 1 unless clear casting is active then cast max rank
```
/run local i = 1 while UnitBuff("player", i) do if UnitBuff("player", i) == "Interface\\Icons\\Spell_Shadow_ManaBurn" then return CastSpellByName"Arcane Missiles" end i = i + 1 end CastSpellByName"Arcane Missiles(Rank 1)"
```
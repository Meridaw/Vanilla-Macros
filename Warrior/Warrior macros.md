## Dont waste consumables macro: (Only use in Combat) (4 => Last bag, 10 slot counting from topleft to bottom right)
```
/script if UnitAffectingCombat("player") then UseContainerItem(4,10) end
```
 

## Startattack macro: (41 being the actionslot)
```
/script if not IsCurrentAction(41) then UseAction(41) end
```
 

## Berserker Rage + Startattack:
```
/cast Berserker Stance
/cast Berserker Rage
/script if not IsCurrentAction(41) then UseAction(41) end
```
 

## Charge macro:
```
/script if not UnitAffectingCombat("player") then CastSpellByName("Battle Stance"); CastSpellByName("Charge"); end
```
 

## Cleave + Startattack:
```
/cast Cleave
/script if not IsCurrentAction(41) then UseAction(41) end
```
 

## Bloodthirst + Startattack:
```
/cast Bloodthirst
/script if not IsCurrentAction(41) then UseAction(41) end
```
 

## Disarm + Startattack:
```
/cast Defensive Stance
/cast Disarm
/script if not IsCurrentAction(41) then UseAction(41) end
```
 

## Execute macro:
```
/script local p=100*UnitHealth("target")/UnitHealthMax("target");if (p>5 or UnitHealth("target")>25000) and UnitMana("player")<26 then CastSpellByName("Berserker Stance"); end; CastSpellByName("Execute");if not IsCurrentAction(41) then UseAction(41) end
```
 

## Juju flurry macro: (Cast self without untargeting the boss)
```
/script UseContainerItem(3,16); SpellTargetUnit("player");
```
 

## Bandage macro:
```
/script UseContainerItem(0,1); SpellTargetUnit("player");
```
 

## Heoric Strike + Startattack:
```
/cast Heroic Strike
/script if not IsCurrentAction(41) then UseAction(41) end
```
 

## Intercept macro + Startattack:
```
/cast Berserker Stance
/cast Intercept
/script if not IsCurrentAction(41) then UseAction(41) end
```
 

## Mocking Blow:
```
/cast Battle Stance
/cast Mocking Blow
```
 

## Overpower:
```
/cast Battle Stance
/cast Overpower
/script if not IsCurrentAction(41) then UseAction(41) end
```
 

## Pummel macro:
```
/cast Berserker Stance
/cast Pummel
```
 

## Switch mainhand weapon macro:
```
/script UseContainerItem(0,2)
```
 

## Thunderclap + Startattack:
```
/cast Battle Stance
/cast Thunder Clap
/script if not IsCurrentAction(41) then UseAction(41) end
```
 

## Whirlwind + Startattack:
```
/cast Berserker Stance
/cast Whirlwind
/script if not IsCurrentAction(41) then UseAction(41) end
```
 

## Shield Bash macro: (22 being the actionslot of your shield)
```
/script UseAction(22); CastSpellByName("Defensive Stance"); CastSpellByName("Shield Bash"); if not IsCurrentAction(41) then AttackTarget() end
```
 

## Battle Stance to Berserker Stance Whirlwind macro:
It does Bloodthirst if you have enough rage and its off cd or getting of cd and then switches stance in order to not waste any rage.
```
/script local a,h,b,c=CastSpellByName,UnitMana("player"),GetActionCooldown(75); if h<=25 or (b+c-GetTime())>1.5 then a("Berserker Stance"); a("Whirlwind") else a("Bloodthirst") end; if not IsCurrentAction(41) then UseAction(41) end
```
 

## Autoattack macro with check for Shadow Command at Nef:
```
/script zu=true;for i=1,2 do GameTooltip:SetUnitDebuff("target", i);if (GameTooltipTextLeft1:GetText() or "")=="Shadow Command" then zu=false end;end if zu then CastSpellByName("Bloodthirst");if not IsCurrentAction(41) then AttackTarget() end;end
```
 

Made by Shino 
## Viper sting / Scorpid sting
```
/run class=UnitClass("target"); if ((class=="Rogue") or (class=="Warrior")) then CastSpellByName("Scorpid Sting"); else CastSpellByName("Viper Sting")end
```
 

## Viper Sting / Serpent Sting
if target is player controlled and has mana cast Viper Sting, else cast Serpent Sting
```
/run if (UnitPowerType('target')==0) and UnitPlayerControlled("target") then CastSpellByName("Viper Sting")else CastSpellByName("Serpent Sting")end
```	
	
	
## Viper sting on trap target without auto shot
```
/run local i,x=1,0 while UnitDebuff("target",i) do if UnitDebuff("target",i)=="Interface\\Icons\\Spell_Frost_ChainsOfIce" then x=1 end i=i+1 end if x==1 then CastSpellByName("Viper Sting")ClearTarget() else CastSpellByName("Viper Sting")end
```


## Viper/Scorpid/Serpent Sting
```
/script class=UnitClass("target") c=CastSpellByName; if UnitIsPlayer("target") and ((class=="Rogue") or (class=="Warrior")) then c("Scorpid Sting") elseif UnitIsPlayer("target") then c("Viper Sting") else c("Serpent Sting"); end
```
## Uses BUFF_1 if the main buff is active, or else uses SPELL_2
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Texture_Name" then x=1 end i=i+1 end if x==0 then CastSpellByName("BUFF") else CastSpellByName("SPELL") end
```
You need to replace "BUFF_TEXTURE" with the TEXTURE of a particular buff and NOT it's name. For example A Rogue's Stealth skill and a Druid's Prowl skill both use the little icon texture called "Ability_Ambush".
Use this site to lookup your buff's texture:
```
http://wowwiki.wikia.com/Queriable_buff_effects
```
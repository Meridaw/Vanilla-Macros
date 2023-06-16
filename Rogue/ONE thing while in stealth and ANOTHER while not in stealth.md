## A macro that will allow you to do ONE thing while in stealth and ANOTHER while not in stealth is like this...
```
/script i=1;m=0;while(UnitBuff("player",i)~=nil) do if(strfind(UnitBuff("player",i),"Ability_Stealth")~=nil) then m=1; end;i=i+1;end; c=CastSpellByName; if(m==1) then c("SPELL_1");else c("SPELL_2");end;
```
You can use this for any Buff/Aura aswell if you simply replace "Ability_Stealth" with the appropriate buff icon texture. eg. "Ability_Stealth" = the little icon of the guy peaking from leaves.

## Use this site for a list of Buff Textures:
```
http://wowwiki.wikia.com/Queriable_buff_effects
```
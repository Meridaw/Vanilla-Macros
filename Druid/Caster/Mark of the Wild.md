## Buff target with Gift of the Wild if Gift of the Wild is missing, then Thorns if Thorns is missing, else Rejuvenation.
```
/run c=CastSpellByName function b(k)for i=1,16 do if strfind(tostring(UnitBuff("target",i)),k)then return 1 end end end if not b("Nature_Regeneration")then c("Gift of the Wild")elseif not b("Nature_Thorns")then c("Thorns")else c("Rejuvenation")end
```


## Buff oneself with Mark of the Wild if Mark of the Wild is missing, then Thorns if Thorns is missing. else Omen of Clarity.
```
/run c=CastSpellByName function b(k)for i=1,16 do if strfind(tostring(UnitBuff("player",i)),k)then return 1 end end end if not b("Nature_Regeneration")then c("Mark of the Wild",1)elseif not b("Nature_Thorns")then c("Thorns",1)else c("Omen of Clarity")end
```


## Adjust buff ranks due to target level
```
/script Pre="Mark of the Wild(Rank " Sp={1,2,14,26,38,50} if (UnitLevel("target") ~= nil and UnitIsFriend("player","target")) then for i=5,1,-1 do if (UnitLevel("target") >= Sp) then CastSpellByName(Pre..i..")") return end end end
```
 

## Mark of the Wild, else Thorns
```
/run local i,x=1,0 while UnitBuff("player",i) do if UnitBuff("player",i)=="Interface\\Icons\\Spell_Nature_Regeneration" then x=1 end i=i+1 end if x==0 then CastSpellByName("Mark of the Wild") else CastSpellByName("Thorns") end
```
 

## Mark of the Wild/Faerie Fire
```
/run if UnitCanAttack("player","target") == 1 then CastSpellByName("Faerie Fire")else CastSpellByName("Mark of the Wild")end
```
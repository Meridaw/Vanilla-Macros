## Arcane Intellect:
```
/run a="Arcane Intellect" b={1,4,18,32,47} c="target" d="(Rank " e=CastSpellByName if (UnitLevel(c) ~= nil and UnitIsFriend("player",c)) then for i=5,1,-1 do if (UnitLevel(c) >= b) then e(a..d..i..")") return end end else e(a,1) end
```


## Arcane Intellect and hide spam: 
```
/run local a,b,c,d,e,u="Arcane Intellect",{1,4,18,32,47},"target","(Rank ",CastSpellByName,UnitLevel if u(c)~=nil and UnitIsFriend("player",c)then for i=5,1,-1 do if(u(c)>=b)then e(a..d..i..")")return end end else e(a,1) end
/run UIErrorsFrame:Hide()
```
 

## Conjure Water:
```
/run a="Conjure Water" b={1,5,15,25,35,45,55} c="target" d="(Rank " e=CastSpellByName if (UnitLevel(c) ~= nil and UnitIsFriend("player",c)) then for i=7,1,-1 do if (UnitLevel(c) >= b) then e(a..d..i..")") return end end else e(a,1) end
```


## Conjure Food:
```
/run a="Conjure Food" b={1,5,15,25,35,45,55} c="target" d="(Rank " e=CastSpellByName if (UnitLevel(c) ~= nil and UnitIsFriend("player",c)) then for i=7,1,-1 do if (UnitLevel(c) >= b) then e(a..d..i..")") return end end else e(a,1) end
```


If you just have 45 water/food change it to
b={1,5,15,25,35,45}
i=6,1,-1
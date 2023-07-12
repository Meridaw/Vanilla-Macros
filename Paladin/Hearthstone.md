## Divine Protection, Hearthstone
```
/run CastSpellByName("Divine Protection") for b=0,4 do for s=1,GetContainerNumSlots(b) do local n=GetContainerItemLink(b,s) if n and strfind(n,"Hearthstone") then UseContainerItem(b,s)  end end end
```


## Divine Shield, else Hearthstone 
Put Hearthstone in the first slot of your backpack for this macro to work
```
/run local i,g=0,GetPlayerBuff; CastSpellByName("Divine Shield(Rank 2)");while not (g(i)==-1) do if (strfind(GetPlayerBuffTexture(g(i)),"Interv")) then UseContainerItem(0,1);end;i=i+1;end
```
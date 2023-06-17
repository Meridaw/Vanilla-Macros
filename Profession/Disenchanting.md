Just mouse over the item you want to disenchant (in your bags only) and run the macro.
```
/run SpellStopTargeting(); local f=GetMouseFocus(); if strfind(tostring(f:GetName()), 'ContainerFrame') then CastSpellByName('Disenchant'); f:Click(); end SpellStopTargeting(); ClearCursor();
```
The way I made it was for default ui, as bagnon uses its own frames. You just simply need to change it to what bagnon frames use.

Just mouse over a slot in the bags and type
```
/run DEFAULT_CHAT_FRAME:AddMessage(GetMouseFocus():GetName())
```
..In this case.. you get something along the lines of 'BagnonItem19' or so.

So just replace 'ContainerFrame' with 'Bagnon',
```
/run SpellStopTargeting(); local f=GetMouseFocus(); if strfind(tostring(f:GetName()), 'Bagnon') then CastSpellByName('Disenchant'); f:Click(); end SpellStopTargeting(); ClearCursor();
```

or just simply remove the if statement which will allow it to be used in any frame which might cause unforeseen issues. (Will cause errors to appear on non-clickable/non-existent frames)
```
/run SpellStopTargeting(); local f=GetMouseFocus(); CastSpellByName('Disenchant'); f:Click(); SpellStopTargeting(); ClearCursor();
``` 
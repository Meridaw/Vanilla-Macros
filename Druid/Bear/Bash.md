## From any stance to bear, cast Bash
```
/run local _, _, active = GetShapeshiftFormInfo(1) if not active or IsControlKeyDown() then for i = 2, 4 do _, _, active = GetShapeshiftFormInfo(i) if active then CastShapeshiftForm(i) return end end CastShapeshiftForm(1) else CastSpellByName("Bash")end
```
## Healing Potion if in BG, else regular
Put potions in 2 different slots, replace `p1` with the BG potion slot id, `p2` with the normal one
```
/run for _,b in {"Warsong Gulch", "Arathi Basin", "Alterac Valley"} do if GetZoneText() == b then UseAction(p1) return end end UseAction(p2)
```
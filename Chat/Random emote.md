## Randomly use a set of emotes
```
/run local a={"roar","charge","attacktarget","gloat"} DoEmote(a[random(table.getn(a))])
```
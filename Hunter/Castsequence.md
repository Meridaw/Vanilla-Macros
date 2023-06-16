## Cycle Hunter's Mark, Serpent Sting, and Concussive Shot
```
/run s={"Hunter's Mark","Serpent Sting","Concussive Shot"} if q==nil then q=0 end q=q+1 if q>getn(s) then q=1 end CastSpellByName(s[q])
```
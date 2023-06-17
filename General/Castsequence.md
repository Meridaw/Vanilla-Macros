This will cast spells in the specified order separated by comma. You can add more until you reach the 255 character limit. It does not respect global cooldown so if you click it faster than 1,5 seconds you will skip a step. Keep that in mind! The following example will cast the following: <br/>
1. Mark of the Wild(Rank 7) <br/>
2. Thorns(Rank 6) <br/>
3. Rejuvenation(Rank 10) <br/>
```
/run s={"Mark of the Wild(Rank 7)","Thorns(Rank 6)","Rejuvenation(Rank 10)"} if q==nil then q=0 end q=q+1 if q>getn(s)then q=1 end CastSpellByName(s[q])
```
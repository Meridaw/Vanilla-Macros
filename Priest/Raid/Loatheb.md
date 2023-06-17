## Sends Next! in yell if you got Corrupt Mind debuff, else Greater Heal 
```
/run function b(k)for i=1,32 do if strfind(tostring(UnitDebuff("player",i)),k)then return 1 end end end if not b("Spell_Shadow_AuraOfDarkness")then CastSpellByName("Greater Heal")else SendChatMessage("Next!", "YELL")end
```
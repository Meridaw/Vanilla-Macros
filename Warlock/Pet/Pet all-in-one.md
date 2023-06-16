## Fire Shield, or Devour Magic if friendly target, else Sacrifice, Seduce target, or Devour Magic self
```
/run if UnitIsFriend("player", "target")then CastSpellByName("Devour Magic")CastSpellByName("Fire Shield")else CastSpellByName("Sacrifice")CastSpellByName("Seduction") CastSpellByName("Devour Magic",1)end
```


## Cast the pet skill that is available if target, if no target pet follows you and casts the pet skill that is available on you
```
/run if(UnitExists("target")) then CastSpellByName("Devour Magic")CastSpellByName("Sacrifice")CastSpellByName("Seduction")CastSpellByName("Fire Shield")else PetFollow() CastSpellByName("Devour Magic",1)CastSpellByName("Sacrifice")end
```
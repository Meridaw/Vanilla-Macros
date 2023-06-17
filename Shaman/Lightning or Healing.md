## Lightning bolt/healing wave
```
/run if UnitCanAttack("player","target") == 1 then CastSpellByName("lightning bolt") else CastSpellByName("healing wave") end
```
 

## Purge/Healing wave(Rank 4)
```
/run if UnitCanAttack("player","target") == 1 then CastSpellByName("Purge") else CastSpellByName("Healing Wave(Rank 4)") end
```
 

## Elemental Mastery, Chain Lightning/Chain Heal
```
/run if UnitCanAttack("player","target") == 1 then CastSpellByName("Elemental Mastery")CastSpellByName("Chain Lightning")else CastSpellByName("Chain Heal") end
```
 

## Nature's Swiftness, Lightning bolt/Healing Wave
```
/run CastSpellByName("Nature's Swiftness") if UnitCanAttack("player","target") == 1 then CastSpellByName("lightning bolt") else CastSpellByName("healing wave")end
```
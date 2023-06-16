## Uber Pet Attack
```
/run if UnitExists("target") then if UnitIsFriend("player","target") then AssistUnit("target");PetAttack();else if UnitExists("pettarget") and UnitIsUnit("target", "pettarget") then PetFollow();else PetAttack();end;end;else PetFollow();end;
```
## Tip: 
Hit the macro on a Friendly Target, it will send your Pet to assist Friendly Target. Hit the macro on a Hostile Target, it will sic your Pet on that Hostile Target. Hit the macro again, it’ll recall your Pet. This works irregardless of your Pet’s Mode (Aggressive/Defensive/Passive).
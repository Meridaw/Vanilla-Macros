Raid marks

/run SetRaidTarget("target", 8) = Skull

/run SetRaidTarget("target", 7) = Cross

/run SetRaidTarget("target", 6) = Square

/run SetRaidTarget("target", 5) = Moon

/run SetRaidTarget("target", 4) = Triangle

/run SetRaidTarget("target", 3) = Purple

/run SetRaidTarget("target", 2) = Circle

/run SetRaidTarget("target", 1) = Star

/run SetRaidTarget("target", 0) = Removes the mark

 

Target raid marked enemy

/run for i=1,13 do TargetNearestEnemy();if GetRaidTargetIndex("target")==X then do return;end;end;end;

Underlined characters: 13 represents the number of mobs to cycle through. Increase it to suit your needs. X represents the number of the raid target index. (8 is skull etc)

 

This one is for skull, change the 8 to something else for different marks.

/run for i=1,18 do if GetRaidTargetIndex('target') == 8 then break end; TargetNearestEnemy(); end 
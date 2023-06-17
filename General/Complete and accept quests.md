## Complete/Accept quests with a keybind 
Not 100% effective if there are more than 1 quest reward
```
/run AcceptQuest()
/run CompleteQuest()
/run i=GetNumQuestChoices() if i<2 then GetQuestReward(1) end
/run SelectAvailableQuest(1)
/run SelectGossipAvailableQuest(1)
/run SelectActiveQuest(1)
/run SelectGossipActiveQuest(1) 
```


## Turn In Quest Items
```
/run SelectGossipAvailableQuest(1); CompleteQuest(); GetQuestReward();
```
Use: This is usable at almost any quest giver with a blue question mark. It’s especially useful for doing Dark Iron Residue turn ins for Thorium Brotherhood faction. Some of these quest givers offer multiple quests. To have the macro select a quest besides the first one, simply change the number in the parentheses.
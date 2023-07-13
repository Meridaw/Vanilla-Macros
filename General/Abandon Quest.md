## Abandon Quest
use to abandon all the quests in your quest log
```
/run for i=1,GetNumQuestLogEntries() do SelectQuestLogEntry(i); SetAbandonQuest(); AbandonQuest(); end
```
Hey guys, I just wanted to share these macros I made a while ago to really speed up the turn in of the 20 WSG marks, since you have to move the mouse around a lot when you turn them in manually.
(The following 2 macros works perfectly for turning in the AB marks as well)


## Macro 1 
click 1 selects the quest, click 2 accepts the quest:
```
/script SelectGossipAvailableQuest(1); AcceptQuest();
```


## Macro 2 
click 1 selects the quest, click 2 completes the quest, click 3 gets the quest reward:
```
/script SelectGossipActiveQuest(1);CompleteQuest(); GetQuestReward();
```


Since there is no way to start the gossip with the NPC you'll have to rightclick the mob to start the gossip.
so basically: Right click mob, press macro 1 twice, right click the npc, press macro 2 three times. Repeat.
You'll want to replace your spells at actionbutton 1 and 2 or similar while doing this.


I made macros for taking the marks from your mailbox as well

## mail-macro 1: 
picks up the item at the first spot in your mailbox
```
/script TakeInboxItem(1)
```

## mail-macro 2: 
deletes the empty mail after have taken the marks
```
/script DeleteInboxItem(1)
```
Be careful when using these two macros guys since you will not get an notification if you accidentally click delete on a mail where you have not yet picked up the marks.
 

I just wanted to add that you can use this macro for any turn in quests, I just used it to turn in coins at Yojamba Isla.

To turn in the 3 different quests at the coin NPC you'll have to use these three different macros:

 

## Turn-in macro 1:
```
/script SelectGossipActiveQuest(1);CompleteQuest(); GetQuestReward();
```


## Turn-in Macro 2:
```
/script SelectGossipActiveQuest(2);CompleteQuest(); GetQuestReward();
```


## Turn-in Macro 3:
```
/script SelectGossipActiveQuest(3);CompleteQuest(); GetQuestReward();
```


Here is a video of me showing off the mark turn-in and mailbox macros. 
```
http://www.youtube.com/watch?v=BQLAK0RL3aw
```
Enjoy ! 
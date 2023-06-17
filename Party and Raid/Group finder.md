## About
This is a macro that aims to slightly enhance "/who whispering".

## What is "/who whispering"?

"/who whispering" is where you get a list of players using the /who command and whisper them. I've always found this method to be the quickest and easiest way to build a group, especially when you're looking for specific roles; notably tanks and healers.

## Setup
 

Create the "set message & reset" macro 
edit the message between the " ":
```
/run lfm_msg= "LF3M RFC: Lv.14+ Tank, Heal, RDPS";lfm_i=1;message(lfm_msg);
```
## Create the "send message" macro:
```
/run if(lfm_i<=GetNumWhoResults()) then lfm_target=GetWhoInfo(lfm_i);SendChatMessage(lfm_msg,"WHISPER",nil,lfm_target);lfm_i=lfm_i+1;else message("Finished who list.");end;
```

## Usage
 

1. Use /who to get a list of players to recruit (ex. /who 18 c-"warrior")<br/>
2. Run the "set message & reset" macro once<br/>
3. Run the "send message" macro repeatedly to whisper each player in the /who list<br/>
- A message will appear when you've finished the list<br/>
4. When you finish the list, repeat steps 1-3 with a new list of different players<br/>
- * Important * If the /who list contains previously whispered names, it will rewhisper them<br/>
- New /who list example: /who 16 c-"warrior"<br/>
- Step 2 must be repeated to reset the macro's list position<br/>
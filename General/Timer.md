## Simple script to track the time elapsed from a set point in time.

1. Clicking the script while holding the Alt key down will begin the timer and state so.
E.g. "Timer Set: [Instance Start]".

2. Clicking the script without any additional keys thereafter will yield the time elapsed.
E.g. "Time Elapsed - [Instance Start]: 00h:01m19s".

If you click the script without holding the Alt key first, you will receive an interface error. If you log off for whatever reason,

your timer will be erased. Change "Say" to whatever channel you want "Party", "Raid", "Guild", etc.
```
/run if IsAltKeyDown() then L1="Instance Start"; T1=GetTime(); M=format("Timer Set [%s]",L1); else N=GetTime(); D=N-T1; M=format("Time Elapsed – [%s]: %02dh:%02dm:%02ds",L1, D/3600,mod((D/60),60), mod(D,60)); end; SendChatMessage(M,"SAY");
```

## About script variables

L1 (Label) – Holds the label for the timer. If you have script space, you can copy this script and change L1 to L2, L3 etc. creating multiple timers each with different labels (Core Hound 1, Core Hound 2 etc.)

T1 (Time) – Holds the base time from which time elapsed is computed. For multiple scripts, change T1 to T2, T3 etc.

M (Message) – Temporary variable to hold message formatting.

N (Now) – Temporary variable to hold the current time. Used in computation.
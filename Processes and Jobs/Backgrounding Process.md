In this challenge we have to resume a suspended process in the background.
## My Solve

**Flag:**pwn.college{Io8XnL9Nd6PoO9Msr0MmkD_f2Vg.QX3QDO0wCN4kjNzEzW}
In this challenge, I first suspended /challenge/run using Ctrl-Z and then resumed it in the background using bg and then launched another copy while the first was running in the background.
```bash
hacker@processes~backgrounding-processes:~$ /challenge/run
^Z
hacker@processes~backgrounding-processes:~$ bg
hacker@processes~backgrounding-processes:~$ /challenge/run
```

## What I Learned
Through this challenge, I was able to learn that bg is used to resume a suspended process in the background.

## Refernces
Did not use any references for this challenge.

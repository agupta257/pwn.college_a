In this challenge we have to resume a suspended process.
## My Solve

**Flag:**pwn.college{MVFlLIoPG4SrYeh_xttGeAtVKtm.QX2QDO0wCN4kjNzEzW}
In this challenge, I first suspended /challenge/run using Ctrl-Z and then resumed it using fg.
```bash
hacker@processes~resuming-processes:~$ /challenge/run
^Z
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{MVFlLIoPG4SrYeh_xttGeAtVKtm.QX2QDO0wCN4kjNzEzW}

## What I Learned
Through this challenge, I was able to learn that fg is used to resume a suspended process

## Refernces
Did not use any references for this challenge.



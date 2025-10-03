In this challenge we have to use the command ps aux to find the name of the command.
## My Solve

**Flag:**pwn.college{EDbaeWfm6DxhfzOmDrNW6SpsJZ0.QX4MDO0wCN4kjNzEzW}
In this challenge, I used the command px aux and then I found  /challenge/16516-run-16589 which gave the flag.
```bash
hacker@processes~listing-processes:~$ /challenge
bash: /challenge: Is a directory
hacker@processes~listing-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  0.0   1056   640 ?        Ss   13:47   0:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-works
root           7  0.0  0.0 231708  2560 ?        S    13:47   0:00 /run/dojo/bin/sleep 6h
root         132  0.0  0.0   4132  2560 ?        S    13:47   0:00 /challenge/16516-run-16589
root         135  0.0  0.0   2744  1600 ?        S    13:47   0:00 sleep 6h
hacker       137  0.0  0.0 231576  3520 pts/0    Ss   13:47   0:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-inte
hacker       143  0.0  0.0 231940  4160 pts/0    S    13:47   0:00 /run/dojo/bin/bash --login
hacker       153  0.0  0.0 233600  3840 pts/0    R+   13:48   0:00 ps aux
hacker@processes~listing-processes:~$  /challenge/16516-run-16589
Yahaha, you found me! Here is your flag:
pwn.college{EDbaeWfm6DxhfzOmDrNW6SpsJZ0.QX4MDO0wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that ps aux gives out the processes that are running and which arent in a user readable format.

## Refernces
Did not use any references for this challenge.

In this challenge we have to kill the /challenge/dont_run process.
## My Solve

**Flag:**pwn.college{ILc9UMQx0AmF6Z_iDpMMej7bTfu.QXyQDO0wCN4kjNzEzW}
In this challenge, I first used ps aux to get a list of all the running processes and then I used the kill command for the /challenge/dont_run process.
```bash
hacker@processes~killing-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.5  0.0   1056   640 ?        Ss   13:57   0:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-works
root           7  0.3  0.0 231708  2560 ?        S    13:57   0:00 /run/dojo/bin/sleep 6h
root         135  0.0  0.0   5204  3200 ?        S    13:57   0:00 su -c /challenge/.launcher hacker
hacker       136  0.0  0.0 231576  3520 ?        Ss   13:57   0:00 /challenge/dont_run
hacker       137  0.0  0.0 231708  2560 ?        S    13:57   0:00 sleep 6h
hacker       139  0.5  0.0 231576  3520 pts/0    Ss   13:57   0:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-inte
hacker       145  0.1  0.0 231940  4160 pts/0    S    13:57   0:00 /run/dojo/bin/bash --login
hacker       154  0.0  0.0 233600  3840 pts/0    R+   13:57   0:00 ps aux
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{ILc9UMQx0AmF6Z_iDpMMej7bTfu.QXyQDO0wCN4kjNzEzW}
```
## What I Learned
Through this challenge, I was able to learn that the kill PID command is used to terminate a running process.

## Refernces
Did not use any references for this challenge.

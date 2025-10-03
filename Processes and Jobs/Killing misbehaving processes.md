In this challenge we have to find and kill /challenge/decoy and run /challenge/run.
## My Solve

**Flag:**pwn.college{Ua4NHvKdrItghDHUTjTJNKfAE6B.0FNzMDOxwCN4kjNzEzW}
In this challenge, I first used ps aux to find the list of the running commands and then I used the kill command to kill the decoy file. Then I worte /chellenge/run and in the other terminal I used the cat command 
for /tmp/flag_fifo. The last flag was the real flag on running /challenge/run again.
```bash
hacker@processes~killing-misbehaving-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.4  0.0   1056   640 ?        Ss   14:16   0:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-works
root           7  0.2  0.0 231708  2560 ?        S    14:16   0:00 /run/dojo/bin/sleep 6h
root         137  0.0  0.0   4132  1280 ?        S    14:16   0:00 /bin/bash /challenge/.init
root         138  0.0  0.0   4132  1280 ?        S    14:16   0:00 /bin/bash /challenge/.init
root         139  0.0  0.0   5204  3520 ?        S    14:16   0:00 su -c exec /challenge/decoy > /tmp/flag_fifo hacker
root         140  0.0  0.0   2744  1600 ?        S    14:16   0:00 sleep 6h
root         141  0.0  0.0   2744  1600 ?        S    14:16   0:00 sleep 6h
hacker       142  0.6  0.0  13516  9280 ?        Ss   14:16   0:00 /usr/bin/python /challenge/decoy
hacker       144  0.5  0.0 231576  3520 pts/0    Ss   14:16   0:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-inte
hacker       150  0.1  0.0 231972  4160 pts/0    S    14:16   0:00 /run/dojo/bin/bash --login
hacker       159  0.0  0.0 233600  3840 pts/0    R+   14:17   0:00 ps aux
hacker@processes~killing-misbehaving-processes:~$ kill 142
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
```
## What I Learned
Through this challenge, I was able to learn the concept of kill, ps aux and FIFO together to get the flag.
## Refernces
Did not use any references for this challenge.

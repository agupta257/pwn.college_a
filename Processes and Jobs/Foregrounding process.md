In this challenge we have to foreground a background process.
## My Solve

**Flag:**pwn.college{oFdcr1bflt21iziGquobB26nbdS.QX4QDO0wCN4kjNzEzW}
In this challenge, I first suspended /challenge/run, then I resumed it in background using bg and then I resumed it in foreground using fg.
```bash
hacker@processes~foregrounding-processes:~$ /challenge/run
^Z
hacker@processes~foregrounding-processes:~$ bg
hacker@processes~foregrounding-processes:~$ fg
```
## What I Learned
Through this challenge, I was able to learn to use bg and fg commands collectively.
## Refernces
Did not use any references for this challenge.

